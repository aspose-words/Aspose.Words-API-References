---
title: Forms2OleControlCollection Class
linktitle: Forms2OleControlCollection
articleTitle: Forms2OleControlCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Ole.Forms2OleControlCollection — решение для эффективного управления объектами Forms2OleControl при обработке документов.
type: docs
weight: 1470
url: /ru/net/aspose.words.drawing.ole/forms2olecontrolcollection/
---
## Forms2OleControlCollection class

Представляет собой коллекцию[`Forms2OleControl`](../forms2olecontrol/) объекты.

Чтобы узнать больше, посетите[Работа с Ole-объектами](https://docs.aspose.com/words/net/working-with-ole-objects/) документальная статья.

```csharp
public class Forms2OleControlCollection : IEnumerable<Forms2OleControl>
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Forms2OleControlCollection](forms2olecontrolcollection/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing.ole/forms2olecontrolcollection/count/) { get; } | Получает количество объектов в коллекции. |
| [Item](../../aspose.words.drawing.ole/forms2olecontrolcollection/item/) { get; } | Получает[`Forms2OleControl`](../forms2olecontrol/) объект по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.ole/forms2olecontrolcollection/getenumerator/)() | Получает перечислитель. |

## Примеры

Показывает, как получить доступ к элементу управления OLE, встроенному в документ, и его дочерним элементам управления.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Фигуры хранят и отображают объекты OLE в теле документа.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Некоторые элементы управления OLE могут содержать дочерние элементы управления, например, тот, что в этом документе с тремя кнопками выбора.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### Смотрите также

* class [Forms2OleControl](../forms2olecontrol/)
* пространство имен [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../)
