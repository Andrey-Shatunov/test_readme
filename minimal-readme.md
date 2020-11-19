# Title

This is an example file with default selections.

## Description

Description .........

## Pre-Install

Please make sure you have Node.js,npm,yarn and the Heroku Toolbelt installed.

## Install


```sh
git clone git@github.com:heroku/node-js-sample.git # or clone your own fork
cd node-js-sample
npm install
npm run-script build 
```


## Configs

This project uses configs ... .env
```
```

## Quick start

```
npm start
```
Your app should now be running on [http://localhost:5000](http://localhost:5000). 

## How to check the work
```
curl http://127.0.0.1:5001/settings
```
You should see an answer
```
{
statusCode: ...,
message: "..."
}
```

# CI/CD
1. Для ветки мастер создан - .github/workflows/master.yml
2. при пуше в мастер выполняется даный workflow, который собирает обаз и пушит его в нашем Docker HUB
3. на сервере запущен - https://github.com/pyouroboros/ouroboros, который проверяет с переодичностью в несколько минут репозиторий. И если образ обновился. он его обновляет на сервере и перезапускает контейнер.
