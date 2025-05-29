---
title: Forms2OleControl.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words para .NET
description: Descubra cómo ajustar fácilmente la propiedad Ancho de Forms2OleControl para ajustar el tamaño del control con precisión en puntos. ¡Mejore su diseño de interfaz de usuario sin esfuerzo!
type: docs
weight: 100
url: /es/net/aspose.words.drawing.ole/forms2olecontrol/width/
---
## Forms2OleControl.Width property

Obtiene o establece el ancho del control en puntos.

```csharp
public double Width { get; set; }
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
