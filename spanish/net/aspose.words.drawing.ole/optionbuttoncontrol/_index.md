---
title: OptionButtonControl Class
linktitle: OptionButtonControl
articleTitle: OptionButtonControl
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Ole.OptionButtonControl, perfecta para crear opciones exclusivas en sus aplicaciones. ¡Mejore la experiencia de usuario hoy mismo!
type: docs
weight: 1510
url: /es/net/aspose.words.drawing.ole/optionbuttoncontrol/
---
## OptionButtonControl class

El control OptionButton permite una única elección en un conjunto limitado de opciones mutuamente excluyentes.

```csharp
public class OptionButtonControl : MorphDataControl
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
| [Selected](../../aspose.words.drawing.ole/optionbuttoncontrol/selected/) { get; set; } | Obtiene o establece un valor booleano que indica esto`OptionButtonControl` está seleccionado o no. |
| override [Type](../../aspose.words.drawing.ole/optionbuttoncontrol/type/) { get; } | Obtiene el tipo de control de Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Obtiene la propiedad Valor subyacente que a menudo representa el estado del control. Por ejemplo, el botón de opción marcado tiene el valor '1' mientras que el desmarcado tiene el valor '0'. El valor predeterminado es una cadena vacía. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Obtiene o establece el ancho del control en puntos. |

## Ejemplos

Muestra cómo seleccionar el botón de opción.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Deseleccionar el primer elemento seleccionado.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// Seleccione el segundo botón de opción.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### Ver también

* class [MorphDataControl](../morphdatacontrol/)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../)
