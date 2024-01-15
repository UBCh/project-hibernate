
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
- реализован ентити-класс  [com.game.entity.Player]()
- реализован enam [com.game.entity.Profession]()
- реализован enam [com.game.entity.Race]()
- реализован репозиторий [com.game.repository.PlayerRepositoryDB]()
- логирование запросов осуществляется p6spy





## особенности реализации com.game.repository.PlayerRepositoryDB
- Метод getAll реализован через NativeQuery — метод получает всех игроков  с учетов параметров: pageNumber - номер страницы, pageSize - количество записей на страницу
- Метод getAllCount реализован через NamedQuery. Возвращает общее количество игроков в базе данных.
- Метод beforeStop позволяет валидно освободить все ресурсы системы.

## запуск на локальной машине
- Сделать fork из [репозитория](https://github.com/UBCh/project-hibernate)
- Скачать свою версию проекта к себе на компьютер.
- Добавить конфигурацию запуска сервера через IDEA
- запустить приложение 
- в Workbench выполнить [скрипт]()
- обновить страницу



