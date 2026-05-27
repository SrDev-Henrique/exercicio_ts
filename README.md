# Exercício TypeScript — EBAC

Projeto introdutório de TypeScript com funções tipadas e configuração básica do compilador.

## O que foi feito

### 1. Funções com tipagem explícita (`index.ts`)

Foram criadas duas funções com parâmetros e retorno tipados:

- **`multiplicar(a: number, b: number): number`** — recebe dois números e devolve o produto deles.
- **`saudacao(nome: string): string`** — recebe um nome e devolve a mensagem `"Olá "` concatenada com o valor informado.

O TypeScript valida em tempo de compilação se os argumentos passados correspondem aos tipos declarados e se o valor retornado é compatível com o tipo de retorno da função.

### 2. Configuração do compilador (`tsconfig.json`)

Foi adicionado um arquivo de configuração do TypeScript com as opções principais:

| Opção | Valor | Descrição |
|-------|-------|-----------|
| `target` | `ES2020` | Versão do JavaScript gerado na compilação |
| `module` | `commonjs` | Sistema de módulos usado no código compilado |
| `strict` | `true` | Ativa verificações rigorosas de tipo |
| `esModuleInterop` | `true` | Melhora compatibilidade com módulos CommonJS/ES |
| `skipLibCheck` | `true` | Ignora checagem de tipos em arquivos `.d.ts` de bibliotecas |
| `forceConsistentCasingInFileNames` | `true` | Exige consistência no uso de maiúsculas/minúsculas nos nomes de arquivo |
| `outDir` | `dist` | Pasta onde o JavaScript compilado será gerado |

O campo `"include": ["*.ts"]` indica que todos os arquivos `.ts` na raiz do projeto devem ser compilados.

## Estrutura do projeto

```
exercicio_ts/
├── index.ts        # Funções tipadas
├── tsconfig.json   # Configuração do TypeScript
└── README.md       # Este arquivo
```

## Como executar

1. Instale o TypeScript globalmente (se ainda não tiver):

   ```bash
   npm install -g typescript
   ```

2. Compile o projeto:

   ```bash
   tsc
   ```

   O JavaScript gerado ficará na pasta `dist/`.

3. (Opcional) Execute o arquivo compilado com Node.js:

   ```bash
   node dist/index.js
   ```

## Conceitos praticados

- Declaração de tipos em parâmetros e retorno de funções
- Tipos primitivos (`number`, `string`)
- Configuração inicial de um projeto TypeScript com `tsconfig.json`
- Compilação de TypeScript para JavaScript
