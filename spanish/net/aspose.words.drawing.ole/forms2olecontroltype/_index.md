---
title: Forms2OleControlType Enum
linktitle: Forms2OleControlType
articleTitle: Forms2OleControlType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.Ole.Forms2OleControlType, que incluye una variedad de tipos de control de Forms 2.0 para una mejor automatización de documentos.
type: docs
weight: 1480
url: /es/net/aspose.words.drawing.ole/forms2olecontroltype/
---
## Forms2OleControlType enumeration

Enumera los tipos de controles de Forms 2.0.

```csharp
public enum Forms2OleControlType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| OptionButton | `0` | Un control de botón de opción. |
| Label | `1` | Un control que muestra texto. |
| Textbox | `2` | Un control que permite al usuario ingresar texto. |
| CheckBox | `3` | Un control que permite al usuario seleccionar o deseleccionar una opción. |
| ToggleButton | `4` | Un control que permite al usuario alternar entre dos estados. |
| SpinButton | `5` | Un control que permite al usuario aumentar o disminuir un valor. |
| ComboBox | `6` | Un control que permite al usuario seleccionar un elemento de una lista. |
| Frame | `7` | Un control que agrupa otros controles. |
| MultiPage | `8` | Un control que muestra varias páginas de contenido. |
| TabStrip | `9` | Un control que permite al usuario cambiar entre múltiples páginas de contenido. |
| CommandButton | `10` | Un botón que activa una acción al hacer clic. |
| Image | `11` | Un control que muestra una imagen. |
| ScrollBar | `12` | Un control que permite al usuario desplazarse por el contenido. |
| Form | `13` | Un contenedor para otros controles. |
| ListBox | `14` | Un control que muestra una lista de elementos. |

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

* espacio de nombres [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../)
