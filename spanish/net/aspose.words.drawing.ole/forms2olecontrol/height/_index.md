---
title: Forms2OleControl.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words para .NET
description: Ajuste fácilmente la altura de Forms2OleControl en puntos para una visualización y funcionalidad óptimas. ¡Mejore su interfaz de usuario con dimensiones de control precisas!
type: docs
weight: 70
url: /es/net/aspose.words.drawing.ole/forms2olecontrol/height/
---
## Forms2OleControl.Height property

Obtiene o establece una altura del control en puntos.

```csharp
public double Height { get; set; }
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
