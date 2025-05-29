---
title: Forms2OleControl.GroupName
linktitle: GroupName
articleTitle: GroupName
second_title: .NET için Aspose.Words
description: Forms2OleControl GroupName özelliğinin, karşılıklı olarak birbirini dışlayan denetimleri zahmetsizce yöneterek kullanıcı deneyimini nasıl geliştirdiğini keşfedin. Daha fazla bilgi edinin!
type: docs
weight: 60
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/groupname/
---
## Forms2OleControl.GroupName property

Karşılıklı olarak birbirini dışlayan denetimlerden oluşan bir grubu belirten bir dize alır veya ayarlar. Varsayılan değer boş bir dizedir.

```csharp
public string GroupName { get; set; }
```

## Örnekler

Bir ActiveX denetiminin özelliklerinin nasıl doğrulanacağını gösterir.

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

    // Bir Çerçeve için GrupAdı ayarlayamayacağınızı unutmayın.
    checkBox.GroupName = "Aspose group name";
}
```

### Ayrıca bakınız

* class [Forms2OleControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
