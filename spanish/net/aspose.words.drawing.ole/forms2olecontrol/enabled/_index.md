---
title: Forms2OleControl.Enabled
second_title: Referencia de API de Aspose.Words para .NET
description: Forms2OleControl propiedad. Devuelve verdadero si el control está en estado habilitado.
type: docs
weight: 30
url: /es/net/aspose.words.drawing.ole/forms2olecontrol/enabled/
---
## Forms2OleControl.Enabled property

Devuelve verdadero si el control está en estado habilitado.

```csharp
public bool Enabled { get; }
```

### Ejemplos

Muestra cómo verificar las propiedades de un control ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual(null, oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
}
```

### Ver también

* class [Forms2OleControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* asamblea [Aspose.Words](../../../)


