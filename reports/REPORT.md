# Лабораторная работа №12. Отчет.

## Задание на лабораторную работу:

- [x] 1. Создать публичный репозиторий с названием **lab12** на сервисе **GitHub**
- [x] 2. Выполнить инструкцию учебного материала
- [x] 3. Ознакомиться со ссылками учебного материала
- [x] 4. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Выполнение работы.
	
В соответствии с последовательностью, определенной заданием на лабораторную работу, были выполнены следующие действия:
- [X] 1. Для успешного выполнения задания создан новый пустой репозиторий lab12 с лицензией MIT.
- [X] 2. Выполнена следующая последовательность команд:

## Tutorial

```ShellSession
$ export GITHUB_USERNAME=woz91
$ export HUNTER_ROOT=`pwd`/projects/hunter
```

```ShellSession
$ vimtutor ru
```

```ShellSession
$ git clone https://github.com/${GITHUB_USERNAME}/lab11 lab12
$ cd lab12
$ git remote remove origin
$ git remote add origin git@github.com:${GITHUB_USERNAME}/lab12
```

```ShellSession
$ vim README.md
:s/lab11/lab12/g
/file<CR>wChaving the path environment variable value **LOG_PATH**<ESC>
:wq
```

```ShellSession
$ vim sources/demo.cpp
Yp3wct>cstdlib<ESC>
/while<CR>ostd::string log_path = std::getenv("LOG_PATH");<ESC>
/"log<CR>
cf"log_path<ESC>
k2dd2kpVj<
:wq
```

```ShellSession
$ pushd $HUNTER_ROOT
$ git config --global hub.protocol https
$ git fork
$ git branch -u ${GITHUB_USERNAME}/master master
$ git release create -m"v0.18.57.1" v0.18.57.1
$ git release show v0.18.57.1
```

```ShellSession
$ wget https://github.com/${GITHUB_USERNAME}/hunter/archive/v0.18.57.1.tar.gz
$ export MYHUNTER_SHA1=`openssl sha1 v0.18.57.1.tar.gz | cut -d'=' -f2 | cut -c2-41`
$ echo $MYHUNTER_SHA1
$ rm -rf v0.18.57.1.tar.gz
```

```ShellSession
$ popd
$ echo $MYHUNTER_SHA1 | pbcopy
$ vim CMakeLists.txt
/SHA1<CR>
wc2w<C-V><ESC>
:wq
```

```ShellSession
$ vim README.md
/lab11<CR>
e<C-A>
ne<C-A>
:wq
```

```ShellSession
$ git add .
$ git commit -m"refactoring"
$ git push origin master
```

```ShellSession
$ travis login --auto
$ travis enable
```

## Report

```ShellSession
$ cd ~/workspace/labs/
$ export LAB_NUMBER=12
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gistup -m "lab${LAB_NUMBER}"
```

- [X] 3. Проведено ознакомление по приведенным ссылкам со следующими материалами по [ex](https://en.wikipedia.org/wiki/Ex_(text_editor)), [vi](https://en.wikipedia.org/wiki/Vi), [hub](https://github.com/github/hub).

- [X] 4. Составлен отчет о работе в формате MD, ссылка отправлена в **slack**.

	
>## Выводы:

>В ходе проделанной работы проведено ознакомление с работой текстового редактора **Vim**, осуществлено редактирование отдельных файлов с использованием **Vim**.
