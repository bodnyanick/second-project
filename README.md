#**БАЗА ЗНАНИЙ НА 20240225**

##**Набор обозначений к командам:**
1. "~" (тильда) - для обращения к домашней директории;
2. "." (одна точка) - для обращения к директории ниже по иерархии;
3. ".." (две точки) - для обращения к директории выше по иерархии;
4. "&&" (два объединения) - для объединения нескольких команд в одной строке;
5. "TAB" (клавиша таб) - для для автозаполнения;
6. стрелки - для переключения по истории команд;

##**Набор известных команд:**
1. **$ CD** - переключение между директроиями;
2. **$ PWD** - определение текущей директории;
3. **$ LS/$ LS -A** - вывод содержания текущей директории/вывод расширенного списка (скрытые файлы и т.п.);  
4. **$ TOUCH** - создание файла через терминал (есть возможность создать файл на уровень иерархии выше, ниже, и т.п. через дополнительные команды в предыдущем разделе);
5. **$ MKDIR/$ MKDIR -P** - создание папки через терминал/создания цепочки папок; 
6. **$ CP** - копирование файлов/папок;
7. **$ MV** - перемещение файлов/папок;
8. **$ CAT** - вывод содержимого текстовых документов на экран терминала;
9. **$ RM** - удаление файлов;
10. **$ RMDIR** - удаление папок;
11. **$ RM -R** - удаление папки со ВСЕМ содержимым;
12. **$ GIT VERSION** - для проверки версии GITа;
13. **$ GIT CONFIG --GLOBAL** - в обучении использовалось для заявления имени юзера и его почты (user.name и user.email);
14. **$ CAT ~/gitconfig** - проверка информации в фале
15. **$ GIT INIT** - слелать папку местонахождения РЕПОЗИТОРИЕМ;
16. **$ RM -RF** - разгитить папку;
17. **$ GIT STATUS** - показать статус репозитория;
18. **$ GIT ADD --ALL** - начать отслеживать ВСЕ файлы в папке;
19. **$ GIT COMMIT -M** - для добавления комментария и, по сути, сохранения изменений;
20. **$ GIT LOG** - для просмотра комментариев;
21. **$ LS -A/.ssh** - проверит SSH-ключи;
22. **$ CLIP <~/.ssh/id_rsa.pub** - скопирует содержание ключа в буфер обмена; 
23. **$ git remote add origin git@github.com:bodnyanick/first-project.git** - для связывания локального и виртуального репозиториев;
24. **$ git remote -v** - для проверки связи репозиториев; 
25. **$ git push origin master/git push** - для первоначальной загрузки данных на виртуальный репозиторий/для повторной загрузки; 
26. **$ ** - 
27. **$ ** - 
28. **$ ** - 
29. **$ ** - 
30. **$ ** - 

##**ХЭШ, ЛОГ, файл HEAD**
###**Хэш**
**Хеш** — основной идентификатор коммита и позволяет узнать его автора, дату и содержимое закоммиченных файлов
*Все хеши, а также таблицу соответствий хеш → информация о коммите Git хранит в папке .git.*
###**Лог**
**Лог** - это история изменения файла, вызывается командой **$ git log**
###**Файл HEAD**
**Файл HEAD** - содержит посследний коммит, т.к. ссыдается на путь **refs/heads/master**

##**Статусы файлов в GIT**
Основные статусы файлов: 
- **untracked** - новые файлы в GIT-репозитории;
- **staged** - файлы, ожидающие коммита (после команды git add);
- **tracked** - все файлы, по которым GIT отслеживает изменения;
- **modified** - файлы, имеющие отличия с последней сохранённой версией.

```mermaid
graph LR;
  "(untracked(неотслеживаемый))"-- "git add" -->"(staged(в списке на коммит)+tracked)"
  "(staged(в списке на коммит)+tracked)"--"git commit"-->"(tracked(отслеживаемый))"
  "(tracked(отслеживаемый))"--"Изменения"-->(modified(изменённый))"
  "(modified(изменённый))"--"git add"-->"(staged(в списке на коммит)+tracked)"
  "(staged(в списке на коммит)+tracked)"--"Изменения"-->"(modified(изменённый))"
``` 



