---
title: TextBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubra la propiedad Tipo TextBoxControl para Forms 2.0, que permite una personalización perfecta del control y mejora la experiencia del usuario en sus aplicaciones.
type: docs
weight: 20
url: /es/net/aspose.words.drawing.ole/textboxcontrol/type/
---
## TextBoxControl.Type property

Obtiene el tipo de control de Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
```

## Ejemplos

Muestra cómo cambiar el texto del control OLE TextBox.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Ver también

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [TextBoxControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../../)
