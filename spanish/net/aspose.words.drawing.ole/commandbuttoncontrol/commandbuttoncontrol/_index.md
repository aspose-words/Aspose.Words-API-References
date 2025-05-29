---
title: CommandButtonControl
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words para .NET
description: Descubra el constructor CommandButtonControl. Cree y personalice fácilmente botones para sus aplicaciones con esta potente instancia de clase.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.ole/commandbuttoncontrol/commandbuttoncontrol/
---
## CommandButtonControl constructor

Inicializa una nueva instancia de[`CommandButtonControl`](../) clase.

```csharp
public CommandButtonControl()
```

## Ejemplos

Muestra cómo insertar un control ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Ver también

* class [CommandButtonControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../../)
