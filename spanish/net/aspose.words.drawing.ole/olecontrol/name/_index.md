---
title: OleControl.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words para .NET
description: Descubra la propiedad OleControl Name para administrar fácilmente el nombre de su control ActiveX. ¡Mejore la funcionalidad y agilice su proceso de desarrollo hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

Obtiene o establece el nombre del control ActiveX.

```csharp
public string Name { get; set; }
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
