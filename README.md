# Testando Google Analytics com VueJS

Este projeto tem como objetivo testar a utilização do Analytics dentro de uma aplicação VueJS.

Foi utilizado como base um codigo que está disponível como exemplo no site do VueJS Examples:
[Link do Repositório](https://vuejsexamples.com/a-simple-todo-application-using-vue-3-composition-api/)

## Primeiros passos

É necesário configurar um domínio dentro da plataforma do [Google Analytics](https://analytics.google.com/) para receber um ID. Com este identificador em mãos acrecente-o no arquivo `main.js` para conseguir fazer o envio de eventos.

```js
import { createApp } from "vue";
import App from "./App.vue";
import VueGtag from "vue-gtag";

createApp(App)
  .use(VueGtag, {
    config: { id: "G-*******" },
  })
  .mount("#app");
```

## Instalando as dependências

```
yarn install
```

### Compilando e iniciando

```
yarn serve
```

## Documentações Úteis

- [Documentação vue-gtag](https://matteo-gabriele.gitbook.io/vue-gtag/)
- [Comparativo de Preços](https://marketingplatform.google.com/intl/pt_BR/about/analytics/compare/)
- [Formato de Eventos no Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs/events?hl=pt_br)
