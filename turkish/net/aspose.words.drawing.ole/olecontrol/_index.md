---
title: Class OleControl
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Ole.OleControl sınıf. OLE ActiveX kontrolünü temsil eder.
type: docs
weight: 1140
url: /tr/net/aspose.words.drawing.ole/olecontrol/
---
## OleControl class

OLE ActiveX kontrolünü temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Ole Nesneleriyle Çalışmak](https://docs.aspose.com/words/net/working-with-ole-objects/) dokümantasyon makalesi.

```csharp
public class OleControl
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | İadeler`doğru` eğer kontrol bir[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | ActiveX denetiminin adını alır veya ayarlar. |

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

* ad alanı [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../)


