---
title: Value
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene la propiedad Valor subyacente que a menudo representa el estado de control. Por ejemplo el botón de opción marcado tiene el valor 1 mientras que no está marcado tiene 0. El valor predeterminado es una cadena vacía.
type: docs
weight: 60
url: /es/net/aspose.words.drawing.ole/forms2olecontrol/value/
---
## Forms2OleControl.Value property

Obtiene la propiedad Valor subyacente que a menudo representa el estado de control. Por ejemplo, el botón de opción marcado tiene el valor '1' mientras que no está marcado tiene '0'. El valor predeterminado es una cadena vacía.

```csharp
public string Value { get; }
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

* class [Forms2OleControl](../../forms2olecontrol)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../forms2olecontrol)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->