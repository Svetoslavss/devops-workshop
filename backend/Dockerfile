FROM node:lts-buster-slim AS development

# Create app directory
WORKDIR /usr/src/app

COPY ./backend/package.json /usr/src/app/package.json
COPY ./backend/package-lock.json /usr/src/app/package-lock.json
RUN npm ci

COPY ./backend /usr/src/app

EXPOSE 3000

CMD [ "npm", "run", "dev" ]

FROM development as dev-envs
RUN apt-get update && apt-get install -y git

RUN useradd -s /bin/bash -m vscode && groupadd docker && usermod -aG docker vscode

# install Docker tools (cli, buildx, compose)
COPY --from=gloursdocker/docker / /
CMD [ "npm", "run", "dev" ]
