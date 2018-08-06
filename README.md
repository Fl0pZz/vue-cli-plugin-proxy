# vue-cli-plugin-proxy

### Work only with Vue CLI RC 11+!!! See this [commit](https://github.com/vuejs/vue-cli/commit/3894a4aba13c88d65319ff849e820ea7833ccb0b)

## Причины создания
Если у вас микросервисная архитектура бека и вы используете прокси во время разработки фронта, то,
вероятно, для отладки или добавления новых фич другие разработчики хотят часть запросов посылать или на тестовый сервер
или на локальные инстанс какого-либо микросервиса. Данный плагин решает именно эту задачу тем, что предоставляет два
файла с настройками: `proxy.config.js` и `proxy.config.local.js`.

`proxy.config.js` нужен для того, чтобы вы определить дефолтные настройки проксирования, а `proxy.config.local.js` нужен,
чтобы часть из них переопределить. При этом `proxy.config.local.js` добавлен в `.gitignore`, это значит что любые изменения
этого файла не попадут в репозиторий

**ВАЖНО!** Плагин не использует настройки `devServer.proxy` из `vue.config.js`. Более того, согласно этому [коммиту]([commit](https://github.com/vuejs/vue-cli/commit/3894a4aba13c88d65319ff849e820ea7833ccb0b))
`vue.config.js` полностью перезапишет настройки прокси.

## proxy.config.*.js
See [vue cli proxy docs](https://cli.vuejs.org/config/#devserver-proxy) and [http-proxy-middleware](https://github.com/chimurai/http-proxy-middleware)
