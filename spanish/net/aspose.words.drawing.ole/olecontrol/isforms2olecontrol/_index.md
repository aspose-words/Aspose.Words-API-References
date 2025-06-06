---
title: OleControl.IsForms2OleControl
linktitle: IsForms2OleControl
articleTitle: IsForms2OleControl
second_title: Aspose.Words para .NET
description: Descubra la propiedad IsForms2OleControl de OleControl, que identifica si su control es un Forms2OleControl, mejorando así la eficiencia de su desarrollo.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.ole/olecontrol/isforms2olecontrol/
---
## OleControl.IsForms2OleControl property

Devuelve`verdadero` Si el control es un[`Forms2OleControl`](../../forms2olecontrol/) .

```csharp
public bool IsForms2OleControl { get; }
```

## Ejemplos

Muestra cómo verificar las propiedades de un control ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.AreEqual("First", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Tenga en cuenta que no es posible establecer un nombre de grupo para un marco.
    checkBox.GroupName = "Aspose group name";
}
```

### Ver también

* class [OleControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../../)
