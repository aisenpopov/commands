git add file

git commit -m "comment"
git commit --amend -m "comment" - коммит вместо последнего коммита

git hist (alias for git log)
git hist --all

git tag tagName
git tag -d oops - удалить тэг

git checkout file - переключение в версию файла file в репозитории

git revert HEAD - отмена коммита
git reset HEAD file - очищает буферную зону к HEAD
reset:
	- Перепишет текущую ветку, чтобы она указывала на нужный коммит
	- Опционально сбросит буферную зону для соответствия с указанным коммитом
	- Опционально сбросит рабочий каталог для соответствия с указанным коммитом
git reset --hard tagName
	- Параметр --hard указывает, что рабочий каталог должен быть обновлен в соответствии с новым head ветки.

git mv fileName dirName:
	Перемещая файлы с помощью git, мы информируем git о 2 вещах
	- Что файл fileName был удален.
	- Что файл dirName/fileName был создан.

Эти команды идентичны:
mkdir lib
git mv hello.html lib

mkdir lib
mv hello.html lib
git add lib/hello.html
git rm hello.html
