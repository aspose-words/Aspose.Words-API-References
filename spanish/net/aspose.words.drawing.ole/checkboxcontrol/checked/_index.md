---
title: CheckBoxControl.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words para .NET
description: Descubra la propiedad CheckBoxControl Checked y administre fácilmente los estados de las casillas de verificación con un simple valor booleano. El valor predeterminado es falso para un control óptimo.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.ole/checkboxcontrol/checked/
---
## CheckBoxControl.Checked property

Obtiene o establece un valor booleano que indica esto[`CheckBoxControl`](../) está marcado o no. El valor predeterminado es`FALSO` .

```csharp
public bool Checked { get; set; }
```

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

* class [CheckBoxControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../../)
