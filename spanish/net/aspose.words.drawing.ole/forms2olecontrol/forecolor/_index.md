---
title: Forms2OleControl.ForeColor
linktitle: ForeColor
articleTitle: ForeColor
second_title: Aspose.Words para .NET
description: Descubra la propiedad ForeColor de Forms2OleControl para personalizar fácilmente el color de primer plano de su control. ¡Mejore su interfaz de usuario con opciones de color personalizadas hoy mismo!
type: docs
weight: 50
url: /es/net/aspose.words.drawing.ole/forms2olecontrol/forecolor/
---
## Forms2OleControl.ForeColor property

Obtiene o establece un color de primer plano del control. El valor predeterminado depende del tipo de control.

```csharp
public Color ForeColor { get; set; }
```

## Ejemplos

Muestra cómo establecer propiedades para el control ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;
oleControl.ForeColor = Color.FromArgb(0x17, 0xE1, 0x35);
oleControl.BackColor = Color.FromArgb(0x33, 0x97, 0xF4);
oleControl.Height = 100.54;
oleControl.Width = 201.06;
```

### Ver también

* class [Forms2OleControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../../)
