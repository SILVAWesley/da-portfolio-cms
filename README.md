<div align="center">

<h3 align="center">Digital Artist Portfolio CMS</h3>

<p>A Strapi a CMS for a digital artist portfolio</p>

<br/>

<nav>
  
[View Portfolio](https://liliagraziely.com)
·
[Report a Bug](https://github.com/SILVAWesley/da-portfolio-cms/issues)

</nav>

</div>

## About this project

As a digital artist, it is very important to have a way to show your work in a way that interested people and companies
can get in touch with you. The art pieces that digital artists want to expose might change from time to time. That being said,
it is very handy for them not having to contact someone who knows how to code to do that. Also, as a developer, getting
requests just to add more art pieces, or change content in the page, can get really frustrating. But also developing a platform
to manage content is very complex and it might be more work than actually possible. <br/> <br/>
That's where this **headless Content Management System (CMS)** built with **Strapi** comes into place. It can manage the showcasing arts,
texts and contact informations in the portfolio while offering:

- Internationalization (in english and brazilian portuguese)
- Image storage in an S3 Bucket
- Full CI/CD with Github Actions and Docker ([checkout the deployment workflow file](.github/workflows/deploy.yaml))
- Deployment on the cloud (AWS)
- Easy local development through the [docker-compose file](docker-compose.yml)
- A postgres database managed by Vercel
- Unit tests using Vitest
- ESLint/Prettier as linting and formating tools
- Husky, commitzen and commitlint to help maintaining the patterns

### Built with

<div align="center">
  
  ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6.svg?style=for-the-badge&logo=TypeScript&logoColor=white)
  ![Svelte](https://img.shields.io/badge/svelte-%23f1413d.svg?style=for-the-badge&logo=svelte&logoColor=white)
  ![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
  ![DaisyUI](https://img.shields.io/badge/daisyui-5A0EF8?style=for-the-badge&logo=daisyui&logoColor=white)
  ![Strapi](https://img.shields.io/badge/strapi-%232E7EEA.svg?style=for-the-badge&logo=strapi&logoColor=white)
  ![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
  ![Playwright](https://img.shields.io/badge/Playwright-2EAD33.svg?style=for-the-badge&logo=Playwright&logoColor=white)
  ![Vitest](https://img.shields.io/badge/Vitest-6E9F18.svg?style=for-the-badge&logo=Vitest&logoColor=white)
  ![Docker](https://img.shields.io/badge/Docker-2496ED.svg?style=for-the-badge&logo=Docker&logoColor=white)
  ![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white)
  ![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
  ![GithubActions](https://img.shields.io/badge/GitHub%20Actions-2088FF.svg?style=for-the-badge&logo=GitHub-Actions&logoColor=white)
  ![NGINX](https://img.shields.io/badge/NGINX-009639.svg?style=for-the-badge&logo=NGINX&logoColor=white)
  
</div>

## Getting Started

You can [access the production release](https://liliagraziely.com). Or, if you want to run the code locally, follow the steps described below.

### Prerequisites

- `node.js >= 18.x & <= 20.x`
- `yarn >= 1.x` or `npm >= 9.x`
- `docker >= 25.x`

### Installing

1. Clone the repository using git

```
git clone https://github.com/SILVAWesley/da-portfolio-cms.git
```

2. Install the dependencies

```
yarn install
```

### Setup .env.compose

1. Create a `.env.compose` file in the `root` directory
2. Fill the file following [the template env file](.env.example)
3. When using docker-compose (as recommended by this tutorial), fill the database connection like this:
   ```
   DATABASE_CLIENT=postgres
   DATABASE_HOST=db
   DATABASE_PORT=5432
   DATABASE_NAME=strapi
   DATABASE_USERNAME=postgres
   DATABASE_PASSWORD=postgres
   DATABASE_SSL=false
   ```

### Start docker compose

1. Run the [docker-compose file](docker-compose.yml):

```
docker compose up
```
