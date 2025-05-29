---
title: CommandButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubra la propiedad Tipo CommandButtonControl para acceder fácilmente a los tipos de control de Forms 2.0, mejorando la funcionalidad de su aplicación y la experiencia del usuario.
type: docs
weight: 20
url: /es/net/aspose.words.drawing.ole/commandbuttoncontrol/type/
---
## CommandButtonControl.Type property

Obtiene el tipo de control de Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CommandButtonControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../../)
