---
title: Caption
second_title: Aspose.Words for .NET API Referansı
description: Denetimin Altyazı özelliğini alır. Varsayılan değer boş bir dizedir.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/caption/
---
## Forms2OleControl.Caption property

Denetimin Altyazı özelliğini alır. Varsayılan değer boş bir dizedir.

```csharp
public string Caption { get; }
```

### Örnekler

ActiveX denetiminin özelliklerinin nasıl doğrulanacağını gösterir.

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

### Ayrıca bakınız

* class [Forms2OleControl](../../forms2olecontrol)
* ad alanı [Aspose.Words.Drawing.Ole](../../forms2olecontrol)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->