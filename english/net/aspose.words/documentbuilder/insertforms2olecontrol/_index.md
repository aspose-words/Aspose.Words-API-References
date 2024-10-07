---
title: DocumentBuilder.InsertForms2OleControl
linktitle: InsertForms2OleControl
articleTitle: InsertForms2OleControl
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertForms2OleControl method. Inserts Forms2OleControl object into current position in C#.
type: docs
weight: 350
url: /net/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder.InsertForms2OleControl method

Inserts [`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/) object into current position.

```csharp
public Shape InsertForms2OleControl(Forms2OleControl forms2OleControl)
```

### Return Value

[`Shape`](../../../aspose.words.drawing/shape/) object that contains passed [`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/)

## Examples

Shows how to insert ActiveX control.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, ((Forms2OleControl)shape.OleFormat.OleControl).Type);
```

### See Also

* property [OleFormat](../../../aspose.words.drawing/shape/oleformat/)
* property [OleControl](../../../aspose.words.drawing/oleformat/olecontrol/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
