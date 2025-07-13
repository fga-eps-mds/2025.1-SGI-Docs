# Django Rest e Next.js

## Histórico de Versões

| Versão | Data       | Modificação                | Autor(es)         |
|--------|------------|----------------------------|-------------------|
|   1.0  | 14/05/2025 | Adiciona relato do dojo   | Danilo Domingo  |

---

Documenta a realização do Dojo de Django Rest e Next.js com o time.

**Data:** 01/05/2025      
**Horário:** 10h        
**Duração:** 2:30h  
**Local:** Discord  
**Elaborador:** Danilo

## Estrutura do Dojo

- **Primeira parte:** uma explicação sobre as stacks e seus funcionamentos.
- **Segunda parte:** foi feito um tutorial utilizando as duas stacks.

## Lista de presença

| Nome                              | Presente (✅/❌) | Justificativa da Ausência               |
|-----------------------------------|-------------------|-----------------------------------------|
| Danilo Domingo                    |     ✅           |                                         |
| Gabi Ribeiro                      |     ❌           |    Motivos Pessoais                                     |
| Jackes Tiago                      |     ✅           |                                         |
| Arthur Gomes Oliveira             |     ✅           |                                         |
| Caio Vilas Boas Miranda           |     ✅           |                                         |
| Carlos Eduardo Figueiredo Coelho  |     ✅           |                      |
| Daniel da Silva Batista           |     ✅           |                                         |
| Guilherme Nascimento Tegnoue      |     ✅           |                                         |
| Gustavo Augusto Da Silva Sousa    |     ✅           |                                         |
| Janio Lucas Pereira Carrilho      |     ✅           |                                         |
| João Guilherme Capozzi Gonçalves  |     ✅           |                                         |
| Joao Guilherme Lima Veras         |     ✅           |                                         |
| Pedro Vieira Antunes              |     ✅           |                                         |

## Explicação das Stacks

### Estrutura Básica do Django

Um projeto Django é composto por vários **apps** que funcionam como módulos. Cada app possui:

- `models.py`: estrutura do banco de dados
- `views.py`: lógica do backend
- `serializers.py`: transformação de dados para API
- `urls.py`: roteamento

---

#### Models

Modelos são classes Python que definem a estrutura das tabelas no banco de dados. Utilizam o ORM do Django.

```python
from django.db import models

class Funcionario(models.Model):
    nome = models.CharField(max_length=100)
    cargo = models.CharField(max_length=50)
    data_admissao = models.DateField()
```

- Cada campo vira uma coluna no banco.  
- Cada instância da classe é um registro (linha).

---

#### Serializers

Os *serializers* convertem objetos Python (como modelos) em JSON e vice-versa. São essenciais para APIs REST.

```python
from rest_framework import serializers
from .models import Funcionario

class FuncionarioSerializer(serializers.ModelSerializer):
    class Meta:
        model = Funcionario
        fields = '__all__'
```

`ModelSerializer` facilita o uso baseado no model.

---

#### Views

As views controlam o comportamento da API. Você pode usar:

**Function-Based Views (FBV)**

```python
from rest_framework.decorators import api_view
from rest_framework.response import Response
from .models import Funcionario
from .serializers import FuncionarioSerializer

@api_view(['GET'])
def listar_funcionarios(request):
    funcionarios = Funcionario.objects.all()
    serializer = FuncionarioSerializer(funcionarios, many=True)
    return Response(serializer.data)
```

**Class-Based Views (CBV)**

```python
from rest_framework import generics

class FuncionarioListCreateView(generics.ListCreateAPIView):
    queryset = Funcionario.objects.all()
    serializer_class = FuncionarioSerializer
```

---

#### URLs

Você precisa registrar suas views nas rotas.

```python
from django.urls import path
from .views import listar_funcionarios

urlpatterns = [
    path('funcionarios/', listar_funcionarios),
]
```

Ou com CBV:

```python
from django.urls import path
from .views import FuncionarioListCreateView

urlpatterns = [
    path('funcionarios/', FuncionarioListCreateView.as_view()),
]
```

---

#### Configuração do Django REST

No `settings.py`, adicione:

```python
INSTALLED_APPS = [
    ...
    'rest_framework',
]
```

### Estrutura do Next.js

```bash
my-app/
├── app/                  # Rotas no novo App Router
│   ├── page.tsx         # Página principal ("/")
│   └── [id]/page.tsx    # Rota dinâmica (ex: "/123")
├── components/          # Componentes reutilizáveis
├── styles/              # Arquivos de estilo (CSS, SCSS, etc)
├── services/            # Funções de acesso à API (Axios, etc)
├── types/               # Tipagens personalizadas (interfaces)
├── public/              # Arquivos estáticos (imagens, ícones)
├── next.config.js       # Configurações do Next.js
└── tsconfig.json        # Configuração do TypeScript
```

---


#### Páginas (Pages)

Cada arquivo `page.tsx` dentro da pasta `app/` representa uma rota.

```tsx
// app/page.tsx
export default function HomePage() {
  return <h1>Bem-vindo ao Dojo!</h1>
}
```

#### Roteamento Dinâmico

```tsx
// app/funcionarios/[id]/page.tsx
import { useParams } from 'next/navigation'

export default function DetalhesFuncionario() {
  const { id } = useParams()
  return <div>Funcionário ID: {id}</div>
}
```

#### Componentes

Componentes são organizados em `components/` e reaproveitados em várias páginas.

```tsx
// components/Header.tsx
export default function Header() {
  return <header><h2>Dojo de Next.js</h2></header>
}
```

---

#### Comunicação com API (Axios + Token)

```ts
// services/axiosInstance.ts
import axios from 'axios'

const axiosInstance = axios.create({
  baseURL: process.env.NEXT_PUBLIC_API_URL,
})

axiosInstance.interceptors.request.use((config) => {
  const token = localStorage.getItem("token")
  if (token) {
    config.headers.Authorization = `Bearer ${token}`
  }
  return config
})

export default axiosInstance
```

**Exemplo de requisição**

```ts
// services/funcionarios.ts
import axiosInstance from './axiosInstance'

export async function getFuncionarios() {
  const response = await axiosInstance.get('/funcionarios/')
  return response.data
}
```

---

#### Tipagens com TypeScript

Crie interfaces para garantir segurança nos dados:

```ts
// types/Funcionario.ts
export interface Funcionario {
  id: number
  nome: string
  cargo: string
  data_admissao: string
}
```

Use no componente:

```tsx
import { Funcionario } from '@/types/Funcionario'

interface Props {
  funcionario: Funcionario
}

export default function CardFuncionario({ funcionario }: Props) {
  return <div>{funcionario.nome} - {funcionario.cargo}</div>
}
```

---

#### Estilização

Você pode usar CSS Modules, SCSS ou qualquer outra abordagem. Exemplo com CSS Modules:

```tsx
// components/Card.module.css
.card {
  padding: 1rem;
  border: 1px solid #ccc;
}
```

```tsx
// components/Card.tsx
import styles from './Card.module.css'

export default function Card({ children }) {
  return <div className={styles.card}>{children}</div>
}
```

---

#### Configuração de Variáveis

No arquivo `.env.local`:

```
NEXT_PUBLIC_API_URL=http://localhost:8000/api
```

Use com `process.env.NEXT_PUBLIC_API_URL`

---

#### Boas Práticas

- Separe lógica de API (`services/`)
- Centralize tipagens em `types/`
- Crie componentes genéricos
- Utilize `useEffect` com responsabilidade para SSR/CSR
- Mantenha a estrutura limpa e previsível


## Tutorial com as Stacks

Foi escolhido um tutorial que utiliza-se as duas stacks, para ser feito durante o dojo e ajudar no intendimento das stacks, foi escolhido um tutorial básico de um menu de restaurante, ele estando disponível no [Dev.TO](https://dev.to/koladev/building-a-fullstack-application-with-django-django-rest-nextjs-3e26).

## Referências

### React & Next.js
- [React JSX](https://pt-br.react.dev/learn/writing-markup-with-jsx) - Documentação oficial sobre JSX, a sintaxe de marcação do React
- [Next.js Documentation](https://nextjs.org/docs) - Documentação completa do Next.js, incluindo tutoriais e guias de API


### Django & Django REST
- [Django Documentation](https://docs.djangoproject.com/pt-br/) - Documentação oficial do Django Framework
- [Django REST Framework](https://www.django-rest-framework.org/) - Documentação completa do Django REST Framework


### API & Conceitos
- [O que é API](https://www.redhat.com/pt-br/topics/api/what-are-application-programming-interfaces) - Explicação da Red Hat sobre APIs
- [O que é REST](https://www.redhat.com/pt-br/topics/api/what-is-a-rest-api) - Guia detalhado sobre APIs REST


### Tutoriais Relacionados
- [Tutorial Django + Next.js](https://dev.to/koladev/building-a-fullstack-application-with-django-django-rest-nextjs-3e26) - Tutorial completo utilizado neste Dojo 
