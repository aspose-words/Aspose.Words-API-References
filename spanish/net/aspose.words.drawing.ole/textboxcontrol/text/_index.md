---
title: TextBoxControl.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: Administre fácilmente el texto de TextBoxControl obtenga o configure su contenido para una interacción fluida del usuario y una funcionalidad mejorada en su aplicación.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.ole/textboxcontrol/text/
---
## TextBoxControl.Text property

Obtiene o establece un texto del control.

```csharp
public string Text { get; set; }
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

* class [TextBoxControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../../)
