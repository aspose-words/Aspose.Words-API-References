---
title: OleControl Class
linktitle: OleControl
articleTitle: OleControl
second_title: .NET için Aspose.Words
description: Gelişmiş işlevsellik için OLE ActiveX denetimlerini uygulamalarınıza sorunsuz bir şekilde entegre etmek amacıyla Aspose.Words.Drawing.Ole.OleControl sınıfını keşfedin.
type: docs
weight: 1500
url: /tr/net/aspose.words.drawing.ole/olecontrol/
---
## OleControl class

OLE ActiveX denetimini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Ole Nesneleriyle Çalışma](https://docs.aspose.com/words/net/working-with-ole-objects/) belgeleme makalesi.

```csharp
public class OleControl
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Geri Döndürür`doğru` eğer kontrol bir[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | ActiveX denetiminin adını alır veya ayarlar. |

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

* ad alanı [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../)
