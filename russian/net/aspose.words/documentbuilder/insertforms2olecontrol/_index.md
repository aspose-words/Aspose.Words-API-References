---
title: DocumentBuilder.InsertForms2OleControl
linktitle: InsertForms2OleControl
articleTitle: InsertForms2OleControl
second_title: Aspose.Words для .NET
description: Легко интегрируйте Forms2OleControl с методом InsertForms2OleControl DocumentBuilder. Расширьте функциональность вашего документа сегодня!
type: docs
weight: 350
url: /ru/net/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder.InsertForms2OleControl method

Вставки[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/) объект в текущую позицию.

```csharp
public Shape InsertForms2OleControl(Forms2OleControl forms2OleControl)
```

### Возвращаемое значение

[`Shape`](../../../aspose.words.drawing/shape/) объект, содержащий переданный[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/)

## Примеры

Показывает, как вставить элемент управления ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Смотрите также

* property [OleFormat](../../../aspose.words.drawing/shape/oleformat/)
* property [OleControl](../../../aspose.words.drawing/oleformat/olecontrol/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
