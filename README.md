This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.tsx`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.ts`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.


## Docker Deployment

Create docker image on windows machine or Mac (Linux x86_64) using the docker file in source code

``bash

#Build docker
docker -D build -t {docker_filename} .
#eg docker -D build -t nextjs-docker-v1.7 .

#Save docker image
docker image save {docker_filename} -o {docker_image_filename}.tar
#eg docker image save nextjs-docker-v1.7 -o unity-web-v1.7.tar

#On linux server (Currently using RHEL)
#Use superuser
sudo su

#List running docker
docker ps

#Stop running docker
docker stop {containerID }

#Remove running docker forcefully
docker rmi -f {container image name}

#Load new docker image file
docker load -i {path_to_docker_image_file}
#eg docker load -i /User/unity-web-v1.7.tar

#Load new docker image file
docker run -d -p 80:3000 {docker_image_file}
#eg docker run -d -p 80:3000 nextjs-docker-v1.7

#check apache processes that are running
ps -ef | grep apache 
```


## Node

``bash
yum install npm

npm install

npx next build

npx next start -p 80
``