# Что нужно сделать, чтобы заработало?

## Для начала на вашу машину надо поставить сам [golangci-lint](https://golangci-lint.run/usage/install/):
* >Поставить его можно как локально, так и через [Docker](https://www.docker.com/) контейнер.
* >Если вы ставите софт на [OC Windows](), то придется ставить через [Git Bash](https://git-scm.com/downloads).

### Настройка для Goland:
* >Так же для начала вам надо будет поставить [расширение *Go Linter*](https://plugins.jetbrains.com/plugin/12496-go-linter)
  > на свою IDE.
* > Так же вам надо будет поставить расширение File Watcher *(вроде как он идет по умолчанию)*.
* > После установки вам надо будет зайти в [File/Settings/Tools/File Watcher]()
  > и там надо добавить новую конфигурацию. Там должна быть встроенная от плагина, но если ее не будет,
  > тогда просто пропишите ```golangci-lint run```.
* > Так же справа вы можете отметить уровень видимости.
* > После положите готовый файл [.golangci.yml]() в корень проекта.
* > Так же в [File/Settings/Tools/File Watcher]() зайдите в пункт Go Linter и укажите путь к линтеру.
* > Так же пропишите в Makefile команду ```lint: golangci-lint run```.

### VSCode
* > Нажмите [F1]() и найдите [Open User Settings JSON]()
* > Пропишите там ```"go.lintTool": "golangci-lint", "go.lintFlags": ["--fast"]```