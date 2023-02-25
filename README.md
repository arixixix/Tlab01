## Laboratory work I

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [ ] 1. Ознакомиться со ссылками учебного материала
- [ ] 2. Выполнить инструкцию учебного материала
- [ ] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Tutorial

```bash
$ export GITHUB_USERNAME=<имя_пользователя>
$ export GIST_TOKEN=<сохраненный_токен>
$ alias edit=<nano|vi|vim|subl>
```

```sh
$ mkdir -p ${GITHUB_USERNAME}/workspace
$ cd ${GITHUB_USERNAME}/workspace
$ pwd
$ cd ..
$ pwd
```

```sh
$ mkdir -p workspace/tasks/
$ mkdir -p workspace/projects/
$ mkdir -p workspace/reports/
$ cd workspace
```

```sh
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
$ tar -xf node-v6.11.5-linux-x64.tar.xz
$ rm -rf node-v6.11.5-linux-x64.tar.xz
$ mv node-v6.11.5-linux-x64 node
```

```sh
$ ls node/bin
$ echo ${PATH}
$ export PATH=${PATH}:`pwd`/node/bin
$ echo ${PATH}
$ mkdir scripts
$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate
```

```sh
$ gem install gist
```

```sh
$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
```

## Report

```sh
$ export LAB_NUMBER=01
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gist REPORT.md
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix))
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix))
- [cd](https://en.wikipedia.org/wiki/Cd_(command))
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix))
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix))
- [echo](https://en.wikipedia.org/wiki/Echo_(command))
- [env](https://en.wikipedia.org/wiki/Env_(shell))
- [ex](https://en.wikipedia.org/wiki/Ex_(editor))
- [file](https://en.wikipedia.org/wiki/File_(command))
- [find](https://en.wikipedia.org/wiki/Find)
- [ls](https://en.wikipedia.org/wiki/Ls)
- [man](https://en.wikipedia.org/wiki/Man_page)
- [mkdir](https://en.wikipedia.org/wiki/Mkdir)
- [mv](https://en.wikipedia.org/wiki/Mv)
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix))
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))
- [pwd](https://en.wikipedia.org/wiki/Pwd)
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix))
- [sed](https://en.wikipedia.org/wiki/Sed)
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix))

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)
- [make](https://en.wikipedia.org/wiki/Make_(software))
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)
- [openssl](https://www.openssl.org)
- [nano](https://www.nano-editor.org)
- [tree](https://linux.die.net/man/1/tree)
- [vim](http://www.vim.org)

## Homework

1. Скачайте библиотеку *boost* с помощью утилиты **wget**. Адрес для скачивания `https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`.
2. Разархивируйте скаченный файл в директорию `~/boost_1_69_0`
3. Подсчитайте количество файлов в директории `~/boost_1_69_0` **не включая** вложенные директории.
4. Подсчитайте количество файлов в директории `~/boost_1_69_0` **включая** вложенные директории.
5. Подсчитайте количество заголовочных файлов, файлов с расширением `.cpp`, сколько остальных файлов (не заголовочных и не `.cpp`).
6. Найдите полный пусть до файла `any.hpp` внутри библиотеки *boost*.
7. Выведите в консоль все файлы, где упоминается последовательность `boost::asio`.
8. Скомпилирутйе *boost*. Можно воспользоваться [инструкцией](https://www.boost.org/doc/libs/1_61_0/more/getting_started/unix-variants.html#or-build-custom-binaries) или [ссылкой](https://codeyarns.com/2017/01/24/how-to-build-boost-on-linux/).
9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию `~/boost-libs`.
10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.
11. Найдите *топ10* самых "тяжёлых".

```
Copyright (c) 2015-2021 The ISC Authors
```

Решение на MacOs

1. <img width="1002" alt="изображение" src="https://user-images.githubusercontent.com/92848880/221350801-936789ac-2f6c-45e8-a6ce-36b6c91d1358.png">

2. -v показывает какие команды делает
   -х записывает на диск с архива / если файл с таким же именем то записывает более новую версию
   -f читает или записывает архив в специализированный файл
   <img width="462" alt="изображение" src="https://user-images.githubusercontent.com/92848880/221351229-2294881f-6a22-415d-b477-dd9575496bdd.png">


3. <img width="400" alt="изображение" src="https://user-images.githubusercontent.com/92848880/221351546-9f14d3cd-9eb3-4ee8-a59e-a89b0c94b961.png">
-а считает скрытые директории

4.<img width="305" alt="изображение" src="https://user-images.githubusercontent.com/92848880/221351652-d8f3c53c-a41d-4a16-88d3-1a867e1d75ee.png">

5. <img width="471" alt="изображение" src="https://user-images.githubusercontent.com/92848880/221351936-2a868f48-dee4-4740-a16c-3ab2a2945da1.png">

6. <img width="591" alt="изображение" src="https://user-images.githubusercontent.com/92848880/221352048-b2485873-318c-4753-875c-601d715ee348.png">

7. <img width="1006" alt="изображение" src="https://user-images.githubusercontent.com/92848880/221352272-e810997e-6353-4762-825c-0d55026b6124.png">

8. <img width="641" alt="изображение" src="https://user-images.githubusercontent.com/92848880/221352413-b3512a8f-ad98-4d54-8934-998f24140dc1.png">


9. <img width="758" alt="изображение" src="https://user-images.githubusercontent.com/92848880/221352571-afb84581-549e-44ec-b30c-e0ac39743792.png">

10. <img width="842" alt="изображение" src="https://user-images.githubusercontent.com/92848880/221352866-0d8c630b-8628-4364-8972-13fa5b4edb77.png">
Ввелась команда ncdu в папке /boost-libs

11. <img width="645" alt="изображение" src="https://user-images.githubusercontent.com/92848880/221353035-361d7482-b2dc-4089-8ff9-7332c4bc8eef.png">
