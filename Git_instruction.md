![Логотип Git](Git-Logo-1788C.png)

# _**Работа с Git**_

## *1. Проверка наличи установленного Git*
В терминале выполнить команду 
```
git --version
```
Если `Git` установлен появиться сообщение с информацией о версий программы, иначе будет сообщение об ошибке.

Пример:


## *2. Установка Git*
Загружаем последнюю версию программы с [сайта](https://git-scm.com/download/win): Устанавливаем с настройками по умолчанию.

## *3. Настройка Git*
После установки необходимо **«представиться»** системе контроля версий. Это нужно сделать всего один раз, и `Git` запомнит вас. Для этого нужно ввести в терминале 2 команды:
```
git config --global user.name "Ваше имя английскими буквами"
```
Например, `git config user.name "Jhon Li"`
```
git config --global user.email ваша почта@example.com
```
Например, `git config user.email jhonli@gmail.com`
   
## *4. Инициализация репозитория*
Для создания нового репозитория используется команда 
```
git init
```
 Команду `git init` выполняют только один раз для первоначальной настройки нового репозитория. Выполнение команды приведет к созданию нового подкаталога `.git` в вашем рабочем каталоге. Кроме того, будет создана новая главная ветка.

 Пример:


## *5. Запись изменений в репозиторий*
```
git status
```
Команда `git status` отображает состояние рабочего каталога и раздела проиндексированных файлов. С ее помощью можно проверить индексацию изменений и увидеть файлы, которые не отслеживаются Git. При этом статус __«Закоммичен»__ не отобразится.

 Пример:


```
git add
```
Команда `git add` используется для добавления изменений в индекс Git. Индекс - это промежуточный слой между рабочей директорией (где находятся ваши файлы) и репозиторием Git (где сохраняются изменения). Когда вы делаете изменения в файлах в рабочей директории, они не автоматически добавляются в индекс. Для того, чтобы добавить изменения в индекс, необходимо использовать команду `git add`.
* Например, `git add Git_instruction.md`, где **Git_instruction.md** название вашего файла.

```
git commit
```

## *8. Игнорирование файлов*
Для того, чтобы исключить из отслеживания в репозитории определённые файлы или папки необходимо создать файл `.gitignore`(обязательно название файла начинается с точки) и записать в него их названия или шаблоны, соответствующие таким файлам или папкам.

## *9. Создание веток в Git*
По умолчанию имя основной ветки в Git - **master**.
Создать ветку можно командой:
```bash
git branch <имя новой ветки>
```
Список веток в репозитори можно посмотреть с помощью команды 
```bash
git branch
```
## *10. Слияние веток и разрешение конфликтов*
```bash
git merge
```
Слияeeeние используется в `Git`, чтобы собрать воедино разветвленную историю. Команда `git merge` выполняет слияние отдельных направлений разработки, созданных с помощью команды `git branch`, в единую ветку. Обратите внимание: все приведенные ниже команды выполняют слияние в текущую ветку, в то время как целевая ветка остается без изменений. Поэтому комаeeewdнда `git merge` часто используется в сочетании с командами `git checkout` (для выбора текущей ветки).Перед слиянием следует предпринять несколько подготовительных действий, чтобы операция прошла без проблем.
* Выполните комаcxcxнду `git status`. Это позволит убедиться, что **HEAD** указывает на ветку, принимающую результаты слияния. При необходимости выполните команду `git checkout <принимающая-ветка>`, чтобы переключитxzfffься на принимающую ветку. Для примера выполним команду `git checkout master`.
* После указанных выше действий по подготовке можете приступать к слиянию. Для этого выполните команду `git merge <название ветки>`, где `<название ветки>` — название ветки, которая будет объединена с принимающей.

При попытке объединить ветки, в которых изменена одна и та же часть того же файла, Git не сможет сделать выбор между версиями. В таком случае операция останавливается прямо перед созданием комcxcxcмита слияния, чтобы пользователь вручную разрешил конфликты. Преимущество слияния в Git заключается в том, что разрешение конфликтов при слиянии проходит по привычной схеме «редактирование — индексирование — коммит». При обнаружении конфликта выполнитxcxе команду git cxcstatus, чтобы увидеть, какие файлы необходимо исправить.

## *9. Создание веток в Git*
По умолчанию имя основной ветки в Git - **master**.
Создать ветку можно командой:
```bash
git branch <имя новой ветки>
```
Список веток в репозитори можно посмотреть с помощью команды 
```bash
git branch
```