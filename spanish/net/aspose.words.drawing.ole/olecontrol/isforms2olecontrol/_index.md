---
title: OleControl.IsForms2OleControl
second_title: Referencia de API de Aspose.Words para .NET
description: OleControl propiedad. Devuelve verdadero si el control es unForms2OleControl .
type: docs
weight: 10
url: /es/net/aspose.words.drawing.ole/olecontrol/isforms2olecontrol/
---
## OleControl.IsForms2OleControl property

Devuelve verdadero si el control es un[`Forms2OleControl`](../../forms2olecontrol/) .

```csharp
public virtual bool IsForms2OleControl { get; }
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

* class [OleControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../olecontrol/)
* asamblea [Aspose.Words](../../../)


