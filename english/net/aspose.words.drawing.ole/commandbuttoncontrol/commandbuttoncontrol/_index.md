---
title: CommandButtonControl
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words for .NET
description: Discover the CommandButtonControl constructor. Effortlessly create and customize buttons for your applications with this powerful class instance.
type: docs
weight: 10
url: /net/aspose.words.drawing.ole/commandbuttoncontrol/commandbuttoncontrol/
---
## CommandButtonControl constructor

Initializes a new instance of [`CommandButtonControl`](../) class.

```csharp
public CommandButtonControl()
```

## Examples

Shows how to insert ActiveX control.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.That(button1.Type, Is.EqualTo(Forms2OleControlType.CommandButton));
```

### See Also

* class [CommandButtonControl](../)
* namespace [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../../)
