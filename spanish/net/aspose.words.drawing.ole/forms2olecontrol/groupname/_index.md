---
title: Forms2OleControl.GroupName
second_title: Referencia de API de Aspose.Words para .NET
description: Forms2OleControl propiedad. Obtiene o establece una cadena que especifica un grupo de controles mutuamente excluyentes. El valor predeterminado es una cadena vacía.
type: docs
weight: 40
url: /es/net/aspose.words.drawing.ole/forms2olecontrol/groupname/
---
## Forms2OleControl.GroupName property

Obtiene o establece una cadena que especifica un grupo de controles mutuamente excluyentes. El valor predeterminado es una cadena vacía.

```csharp
public string GroupName { get; set; }
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

* class [Forms2OleControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* asamblea [Aspose.Words](../../../)


