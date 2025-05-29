---
title: TextBoxControl Class
linktitle: TextBoxControl
articleTitle: TextBoxControl
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Ole.TextBoxControl para mostrar fácilmente texto organizado a partir de datos o entradas del usuario. ¡Mejore su gestión de documentos hoy mismo!
type: docs
weight: 1520
url: /es/net/aspose.words.drawing.ole/textboxcontrol/
---
## TextBoxControl class

El control TextBox muestra texto de un conjunto organizado de datos o de una entrada del usuario.

```csharp
public class TextBoxControl : MorphDataControl
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Obtiene o establece un color de fondo del control. El valor predeterminado depende del tipo de control. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Obtiene o establece una propiedad Caption del control. El valor predeterminado es una cadena vacía. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Obtiene la colección de controles secundarios inmediatos. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Devuelve`verdadero` si el control está en estado habilitado. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Obtiene o establece un color de primer plano del control. El valor predeterminado depende del tipo de control. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Obtiene o establece una cadena que especifica un grupo de controles mutuamente excluyentes. El valor predeterminado es una cadena vacía. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Obtiene o establece una altura del control en puntos. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Devuelve`verdadero` Si el control es un[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Obtiene o establece el nombre del control ActiveX. |
| [Text](../../aspose.words.drawing.ole/textboxcontrol/text/) { get; set; } | Obtiene o establece un texto del control. |
| override [Type](../../aspose.words.drawing.ole/textboxcontrol/type/) { get; } | Obtiene el tipo de control de Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Obtiene la propiedad Valor subyacente que a menudo representa el estado del control. Por ejemplo, el botón de opción marcado tiene el valor '1' mientras que el desmarcado tiene el valor '0'. El valor predeterminado es una cadena vacía. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Obtiene o establece el ancho del control en puntos. |

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

* class [MorphDataControl](../morphdatacontrol/)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../)
