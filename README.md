
## задание
- есть готовый [проект](https://github.com/vasylmalik/project-hibernate-1),с реализованной админ-панелью для rpg для серверного API,а сервере в качестве хранилища использовалась Map .
- задача: написать альтернативную реализацию слоя репозитория с использованием Hibernate.

## Перечень необходимого установленного ПО

* **IntelliJ IDEA Ultimate**
* **Java 18**
* **Tomcat.9**
* **Workbench**


## использовано
- MAVEN
- hibernate
- p6spy
- mySql



## реализовано
- создана БД "rpg"
- реализован ентити-класс  [com.game.entity.Player](https://github.com/UBCh/project-hibernate/blob/master/src/main/java/com/game/entity/Player.java)
- реализован enam [com.game.entity.Profession](https://github.com/UBCh/project-hibernate/blob/master/src/main/java/com/game/entity/Profession.java)
- реализован enam [com.game.entity.Race](https://github.com/UBCh/project-hibernate/blob/master/src/main/java/com/game/entity/Race.java)
- реализован репозиторий [com.game.repository.PlayerRepositoryDB](https://github.com/UBCh/project-hibernate/blob/master/src/main/java/com/game/repository/PlayerRepositoryDB.java)
- логирование запросов осуществляется p6spy
- реализован функционал создание игрока
- реализован функционал удаление игрока
- реализован функционал редактирование игрока





## особенности реализации com.game.repository.PlayerRepositoryDB
- Метод getAll реализован через NativeQuery — метод получает всех игроков  с учетов параметров: pageNumber - номер страницы, pageSize - количество записей на страницу
- Метод getAllCount реализован через NamedQuery. Возвращает общее количество игроков в базе данных.
- Метод beforeStop позволяет валидно освободить все ресурсы системы.

## запуск на локальной машине
- Сделать fork из [репозитория](https://github.com/UBCh/project-hibernate)
- Скачать свою версию проекта к себе на компьютер.
- Добавить конфигурацию запуска сервера через IDEA
- запустить приложение 
- в Workbench выполнить [скрипт](https://github.com/UBCh/project-hibernate/blob/master/src/main/resources/init.sql)
- обновить страницу



