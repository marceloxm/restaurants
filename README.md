# 🍽️ Buscador de Restaurantes (ReactJS + Google Maps & Places API)

## 📖 Sobre o Projeto

O **Buscador de Restaurantes** é uma aplicação web desenvolvida em **ReactJS** que integra a **Google Maps JavaScript API** e a **Google Places API** para localizar estabelecimentos próximos e exibir informações detalhadas em um mapa interativo, inspirado no serviço oficial de busca do Google.

O projeto foi desenvolvido como parte de um desafio prático da **[Digital Innovation One (DIO)](https://dio.me)**, explorando componentização avançada, estilização via CSS-in-JS, gerenciamento de estado global e consumo de APIs de geolocalização.

---

## ✨ Funcionalidades

- **Mapa Interativo (Google Maps):** Exibição da localização atual do usuário (via geolocalização do navegador) com marcadores dinâmicos apontando os restaurantes encontrados na região.
- **Busca Inteligente por Termos:** Campo de pesquisa para filtrar restaurantes por nome, especialidade ou tipo de culinária (ex.: *pizzaria*, *hambúrguer*, *comida japonesa*).
- **Carrossel de Destaques:** Slider horizontal exibindo os principais restaurantes próximos com foto e nome.
- **Lista Detalhada de Resultados:** Cards laterais contendo nome do restaurante, avaliação em estrelas, endereço completo e foto do local.
- **Modal de Detalhes do Restaurante:** Ao clicar em um restaurante na lista ou no carrossel, abre um modal com informações completas obtidas via Google Places Details (telefone, endereço, avaliações e status de funcionamento: *Aberto agora* ou *Fechado*).
- **Skeleton Loading:** Efeito de carregamento visual (*skeletons*) enquanto os dados da API do Google estão sendo requisitados.

---

## 🛠️ Tecnologias Utilizadas

Com base na estrutura do repositório (`package.json`, `yarn.lock`, `jsconfig.json`, `prettier.config.js`), o projeto utiliza:

- **[ReactJS](https://react.dev):** Biblioteca principal para construção da interface de usuário baseada em componentes.
- **Google Maps & Places API (`google-maps-react`):** Integração de mapas interativos, marcadores e busca de estabelecimentos.
- **[Redux](https://js.org) & React-Redux:** Gerenciamento centralizado do estado dos restaurantes retornados e do estabelecimento selecionado.
- **[Styled Components](https://styled-components.com):** Estilização modular por componente (CSS-in-JS).
- **[Material UI](https://mui.com) & React Slick:** Componentes de interface (como avaliação por estrelas e inputs) e carrossel de imagens.
- **[Prettier](https://prettier.io) (`prettier.config.js`):** Padronização automática da formatação do código.
- **[Yarn](https://yarnpkg.com) / npm:** Gerenciamento de pacotes e scripts de execução.

---

## 📂 Estrutura de Diretórios

```text
restaurants/
├── public/               # Arquivos estáticos e index.html
├── src/                  # Código-fonte React (components, pages, redux, assets, theme)
├── jsconfig.json         # Configuração de caminhos absolutos (imports limpos a partir de src/)
├── package.json          # Dependências do projeto e scripts de execução
├── prettier.config.js    # Regras de formatação de código
├── yarn.lock             # Árvore exata das versões instaladas via Yarn
└── README.md             # Documentação do projeto
```

---

## 🚀 Como Executar o Projeto na Sua Máquina

### Pré-requisitos

Antes de começar, certifique-se de ter:
- **[Node.js](https://nodejs.org)** (versão LTS recomendada)
- **[Yarn](https://yarnpkg.com)** (recomendado, pois o projeto utiliza `yarn.lock`) ou **npm**
- **[Git](https://git-scm.com)**
- **Chave de API do Google Cloud (API Key)** com as seguintes APIs habilitadas no [Google Cloud Console](https://google.com):
  - **Maps JavaScript API**
  - **Places API**

---

### Passo a passo

1. **Clone o repositório:**
   ```bash
   git clone https://github.com
   ```

2. **Acesse a pasta do projeto:**
   ```bash
   cd restaurants
   ```

3. **Instale as dependências:**
   Utilizando o Yarn:
   ```bash
   yarn install
   ```
   *(Ou, caso prefira utilizar o npm: `npm install`)*

4. **Configure a Chave da API do Google (Variável de Ambiente):**
   - Na raiz do projeto, crie um arquivo chamado `.env` (caso ainda não exista).
   - Adicione a sua chave de API do Google Maps/Places conforme configurado no código (geralmente `REACT_APP_GOOGLE_API_KEY`):
     ```env
     REACT_APP_GOOGLE_API_KEY=SUA_CHAVE_API_DO_GOOGLE_AQUI
     ```
   > **Nota:** Sem uma chave válida com as APIs *Maps JavaScript* e *Places* ativadas, o mapa exibirá um aviso de erro de autenticação do Google e não carregará os restaurantes.

5. **Inicie o servidor de desenvolvimento:**
   Utilizando o Yarn:
   ```bash
   yarn start
   ```
   *(Ou com npm: `npm start`)*

6. **Acesse a aplicação no navegador:**
   Abra `http://localhost:3000/` e permita o acesso à sua localização quando o navegador solicitar para visualizar os restaurantes próximos à sua região.

---

## 📦 Gerando Build de Produção

Para compilar e otimizar os arquivos da aplicação para publicação em produção, execute:

```bash
yarn build
```
*(Ou `npm run build`)*

Os arquivos finais serão gerados dentro da pasta `build/`.

---

## 🤝 Contribuição

Contribuições são sempre bem-vindas! Se você quiser melhorar este projeto:

1. Faça um **Fork** deste repositório.
2. Crie uma **Branch** para sua melhoria (`git checkout -b feature/NovaFuncionalidade`).
3. Faça o **Commit** das suas alterações (`git commit -m 'Adiciona nova funcionalidade'`).
4. Faça o **Push** para a branch (`git push origin feature/NovaFuncionalidade`).
5. Abra um **Pull Request**.

---

## 👨‍💻 Autor

Desenvolvido por **[marceloxm](https://github.com/marceloxm)** durante os estudos na **Digital Innovation One (DIO)**.
