---
title: OleControl.Name
second_title: Referencia de API de Aspose.Words para .NET
description: OleControl propiedad. Obtiene o establece el nombre del control ActiveX.
type: docs
weight: 20
url: /es/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

Obtiene o establece el nombre del control ActiveX.

```csharp
public string Name { get; set; }
```

### Ejemplos

Muestra cómo verificar las propiedades de un control ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Tenga en cuenta que no puede configurar GroupName para un marco.
    checkBox.GroupName = "Aspose group name";
}
```

### Ver también

* class [OleControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../olecontrol/)
* asamblea [Aspose.Words](../../../)


