# Установка Julia и JupyterLab (Windows)

Для работы дома. В кабинете всё установлено.

Команды вводятся в командной строке: Win+R → `cmd` → Enter.

## 1. uv

```
winget install --id astral-sh.uv -e --source winget --accept-source-agreements --accept-package-agreements
```

Закройте командную строку и откройте заново.

## 2. JupyterLab

```
uv tool install jupyterlab --python 3.12
uv tool update-shell
```

Закройте командную строку и откройте заново.

## 3. Julia 1.11

```
winget install --id Julialang.Juliaup -e --source winget --accept-source-agreements --accept-package-agreements
```

Закройте командную строку, откройте заново и выполните:

```
juliaup add 1.11
juliaup default 1.11
```

## 4. IJulia

Запустите Julia командой `julia`. В строке `julia>` введите:

```julia
using Pkg
Pkg.add("IJulia")
exit()
```

## 5. Запуск JupyterLab

```
cd /d D:\Julia
jupyter-lab
```

`D:\Julia` — папка с блокнотами, можно указать любую. Команда `jupyter-lab` пишется через дефис.
Окно командной строки не закрывайте, пока работаете в JupyterLab.

## Ярлык на рабочем столе

1. Правая кнопка мыши на рабочем столе → Создать → Ярлык.
2. Расположение объекта: `%USERPROFILE%\.local\bin\jupyter-lab.exe`, имя — `JupyterLab`.
3. Правая кнопка мыши на ярлыке → Свойства → «Рабочая папка»: папка с блокнотами, например `D:\Julia`.

## Без установки: Google Colab

1. Откройте colab.research.google.com и войдите в аккаунт Google.
2. Файл → Загрузить блокнот.
3. Среда выполнения → Сменить среду выполнения → Julia.
