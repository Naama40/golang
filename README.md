```go doc fmt.Printf```

```go doc fmt```

```godoc -http=:8001```

```go get -v github.com/mactsouk/go/simpleGitHub```

Загруженные файлы вы найдете в следующем каталоге:

```$ ls -l ~/go/src/github.com/mactsouk/go/simpleGitHub/```

Однако команда go get также компилирует пакет. Соответствующие файлы размещаются здесь:

```$ ls -l ~/go/pkg/darwin_amd64/github.com/mactsouk/go/simpleGitHub.a```

Временные файлы загруженного Go-пакета можно удалить:

```go clean -i -v -x github.com/mactsouk/go/simpleGitHub```

Аналогичным образом с помощью UNIX-команды rm(1) можно удалить весь загруженный и размещенный на локальном компьютере Go-пакет, чтобы удалить его исходный Go-код после использования go clean:
```
$ go clean -i -v -x github.com/mactsouk/go/simpleGitHub 
$ rm -rf ~/go/src/github.com/mactsouk/go/simpleGitHub
```

Файл конфигурации rsyslogd(8) обычно называется rsyslog.conf и находится в /etc. Содержимое файла конфигурации rsyslog.conf, без учета строк с коммен- тариями и строк, начинающихся с $, может выглядеть следующим образом:

```
grep -v '^#' /etc/rsyslog.conf | grep -v '^$' | grep -v '^\$'
```