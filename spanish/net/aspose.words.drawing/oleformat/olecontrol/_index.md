---
title: OleFormat.OleControl
linktitle: OleControl
articleTitle: OleControl
second_title: Aspose.Words para .NET
description: Descubra la propiedad OleFormat OleControl para acceder a los objetos de control ActiveX. Desbloquee funciones mejoradas e integración para sus aplicaciones OLE.
type: docs
weight: 60
url: /es/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

Obtiene`OleControl` Objetos si este objeto OLE es un control ActiveX. De lo contrario, esta propiedad es nula.

```csharp
public OleControl OleControl { get; }
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

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
