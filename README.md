О приложении

[Demo](http://todo-oleg.herokuapp.com)

Все записи постоянно хранятся в localStorage браузера.
Приложение не требует соединения с сервером. Но, когда сервер доступен - открывается WebSocket соединение и все данные синхронизируются. 

При возникновении конфликтов всегда применяются только самые новые данные, за исключением удаления. 
Например, есть offline клиент a и online клиент b. Изменяем(меняем статус или текст, не удаляем) todo#1 на клиенте a, затем изменяем(меняем статус или текст, не удаляем) todo#1 на клиенте b. После перехода клиента a в online, на всех клиентах будут изменения с клиента b, так как они самые новые. В случае удаления на клиенте a, todo#1 удалится со всех клиентов.

В версию 1.0 войдет:
* рефикторинг кода
* удаление будет производится аналогично изменению
* оптимизация и исправление багов
