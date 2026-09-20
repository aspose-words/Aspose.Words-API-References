---
title: "Класс Aspose::Words::Layout::LayoutEnumerator"
linktitle: "LayoutEnumerator"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Layout::LayoutEnumerator. Перечисляет объекты разметки страниц документа. Вы можете использовать этот класс для обхода модели разметки страниц. Доступные свойства: тип, геометрия, текст и индекс страницы, где объект отображается, а также общая структура и взаимосвязи. Используйте комбинацию GetEntity() и Current, чтобы перейти к объекту, соответствующему узлу документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class


Перечисляет объекты разметки страниц документа. Вы можете использовать этот класс для обхода модели разметки страниц. Доступные свойства: тип, геометрия, текст и индекс страницы, где объект отображается, а также общая структура и взаимосвязи. Используйте комбинацию [GetEntity()](../) и [Current](./get_current/), чтобы перейти к объекту, соответствующему узлу документа. Чтобы узнать больше, посетите статью документации [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutEnumerator : public System::Object,
                         public System::Details::EnumeratorBasedIterator<System::SharedPtr<System::Object>>,
                         private System::Details::IteratorPointerUpdater<System::SharedPtr<System::Object>, false>
```

## Методы

| Метод | Описание |
| --- | --- |
| [CloneIterator](./cloneiterator/)() const override |  |
| [get_Current](./get_current/)() const | Получает или задает текущую позицию в модели разметки страниц. Это свойство возвращает непрозрачный объект, который соответствует текущему объекту разметки. |
| [get_Document](./get_document/)() const | Получает документ, который перечисляется этим экземпляром. |
| [get_Kind](./get_kind/)() | Получает тип текущей сущности. Это может быть пустая строка, но никогда не **null**. |
| [get_PageIndex](./get_pageindex/)() | Получает индекс страницы (начиная с 1), содержащей текущую сущность. |
| [get_Rectangle](./get_rectangle/)() | Возвращает ограничивающий прямоугольник текущей сущности относительно левого верхнего угла страницы (в пунктах). |
| [get_Text](./get_text/)() | Получает текст текущей сущности span. Выбрасывает исключение для других типов сущностей. |
| [get_Type](./get_type/)() | Получает тип текущей сущности. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Получает именованное свойство сущности. |
| [IncrementIterator](./incrementiterator/)() override |  |
| [InitializeIterator](./initializeiterator/)() override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutEnumerator](./layoutenumerator/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Инициализирует новый экземпляр этого класса. |
| [MoveFirstChild](./movefirstchild/)() | Переходит к первой дочерней сущности. |
| [MoveLastChild](./movelastchild/)() | Переходит к последней дочерней сущности. |
| [MoveNext](./movenext/)() | Переходит к следующей соседней сущности в визуальном порядке. При переборе строк абзаца, разбитого на страницы, этот метод не переходит к следующей странице, а переходит к следующей сущности на той же странице. |
| [MoveNextLogical](./movenextlogical/)() | Переходит к следующей соседней сущности в логическом порядке. При переборе строк абзаца, разбитого на страницы, этот метод переходит к следующей строке, даже если она находится на другой странице. |
| [MoveParent](./moveparent/)() | Переходит к родительской сущности. |
| [MoveParent](./moveparent/)(Aspose::Words::Layout::LayoutEntityType) | Переходит к родительской сущности указанного типа. |
| [MovePrevious](./moveprevious/)() | Переходит к предыдущей соседней сущности. |
| [MovePreviousLogical](./movepreviouslogical/)() | Переходит к предыдущей соседней сущности в логическом порядке. При переборе строк абзаца, разбитого на страницы, этот метод переходит к предыдущей строке, даже если она находится на другой странице. |
| [Reset](./reset/)() | Перемещает перечислитель на первую страницу документа. |
| [set_Current](./set_current/)(const System::SharedPtr\<System::Object\>\&) | Сеттер для [Aspose::Words::Layout::LayoutEnumerator::get_Current](./get_current/). |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
