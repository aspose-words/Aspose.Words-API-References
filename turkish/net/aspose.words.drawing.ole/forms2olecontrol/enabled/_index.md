---
title: Forms2OleControl.Enabled
second_title: Aspose.Words for .NET API Referansı
description: Forms2OleControl mülk. Denetim etkin durumdaysa true değerini döndürür.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/enabled/
---
## Forms2OleControl.Enabled property

Denetim etkin durumdaysa true değerini döndürür.

```csharp
public bool Enabled { get; }
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

* class [Forms2OleControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* toplantı [Aspose.Words](../../../)


