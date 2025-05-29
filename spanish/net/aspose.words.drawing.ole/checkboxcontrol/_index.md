---
title: CheckBoxControl Class
linktitle: CheckBoxControl
articleTitle: CheckBoxControl
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Ole.CheckBoxControl para alternar fácilmente los valores de las casillas de verificación y mejorar la automatización de sus documentos con una integración perfecta.
type: docs
weight: 1440
url: /es/net/aspose.words.drawing.ole/checkboxcontrol/
---
## CheckBoxControl class

El control CheckBox alterna un valor.

```csharp
public class CheckBoxControl : MorphDataControl
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Obtiene o establece un color de fondo del control. El valor predeterminado depende del tipo de control. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Obtiene o establece una propiedad Caption del control. El valor predeterminado es una cadena vacía. |
| [Checked](../../aspose.words.drawing.ole/checkboxcontrol/checked/) { get; set; } | Obtiene o establece un valor booleano que indica esto`CheckBoxControl` está marcado o no. El valor predeterminado es`FALSO` . |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Obtiene la colección de controles secundarios inmediatos. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Devuelve`verdadero` si el control está en estado habilitado. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Obtiene o establece un color de primer plano del control. El valor predeterminado depende del tipo de control. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Obtiene o establece una cadena que especifica un grupo de controles mutuamente excluyentes. El valor predeterminado es una cadena vacía. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Obtiene o establece una altura del control en puntos. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Devuelve`verdadero` Si el control es un[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Obtiene o establece el nombre del control ActiveX. |
| override [Type](../../aspose.words.drawing.ole/checkboxcontrol/type/) { get; } | Obtiene el tipo de control de Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Obtiene la propiedad Valor subyacente que a menudo representa el estado del control. Por ejemplo, el botón de opción marcado tiene el valor '1' mientras que el desmarcado tiene el valor '0'. El valor predeterminado es una cadena vacía. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Obtiene o establece el ancho del control en puntos. |

## Observaciones

Tiene tres estados posibles: seleccionado, borrado y ni seleccionado ni borrado, es decir, una combinación de estados activado y desactivado.

## Ejemplos

Muestra cómo cambiar el estado del control CheckBox.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Ver también

* class [MorphDataControl](../morphdatacontrol/)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../)
