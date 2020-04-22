[Главная](../main.md)

# Сообщения

Принцип работы с сообщениями одинаков с [диалогами](dialog.md).

Для работы с сообщениями, необходимо подключить к WidgetModel реализацию
абстрактного класса MessageController. Например MaterialMessageController.
Для показа сообщения необходимо вызвать метод `_msgController.show(type, msg: “message“)`.
По умолчанию кастомизировать внешний вид сообщения не обязательно, оно принимает вид стандартного снэка.

Для кастомизации внешнего вида сообщения используется mixin CustomSnackBarOwner.
Данная сущность реализуется на необходимом экране и подключается к MessageController, 
который используется для отображения диалогов в WidgetModel. Таким образом кастомизация внешнего вида
сообщения происходит на ui слое, а обработка логики в WidgetModel, тем самым сохраняя принцип 
разделения ответственности.

Реализация логики вызова сообщения происходит только в сущности WidgetModel.