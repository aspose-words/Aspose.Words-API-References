---
title: Forms2OleControl.ChildNodes
second_title: Aspose.Words for .NET API Referansı
description: Forms2OleControl mülk. Anlık alt kontrollerin toplanmasını alır.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/childnodes/
---
## Forms2OleControl.ChildNodes property

Anlık alt kontrollerin toplanmasını alır.

```csharp
public virtual Forms2OleControlCollection ChildNodes { get; }
```

### Notlar

İadeler`hükümsüz` eğer bu kontrol çocuk sahibi olamazsa.

### Örnekler

ActiveX denetiminin özelliklerinin nasıl doğrulanacağını gösterir.

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

    // Bir Çerçeve için GrupAdı'nı ayarlayamayacağınızı unutmayın.
    checkBox.GroupName = "Aspose group name";
}
```

### Ayrıca bakınız

* class [Forms2OleControlCollection](../../forms2olecontrolcollection/)
* class [Forms2OleControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* toplantı [Aspose.Words](../../../)


