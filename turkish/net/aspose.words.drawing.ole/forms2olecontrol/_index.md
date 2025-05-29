---
title: Forms2OleControl Class
linktitle: Forms2OleControl
articleTitle: Forms2OleControl
second_title: .NET için Aspose.Words
description: Microsoft Forms 2.0 OLE denetimlerini uygulamalarınıza sorunsuz bir şekilde entegre etmek için çözümünüz olan Aspose.Words.Drawing.Ole.Forms2OleControl sınıfını keşfedin.
type: docs
weight: 1460
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Microsoft Forms 2.0 OLE denetimini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Ole Nesneleriyle Çalışma](https://docs.aspose.com/words/net/working-with-ole-objects/) belgeleme makalesi.

```csharp
public abstract class Forms2OleControl : OleControl
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Denetimin arka plan rengini alır veya ayarlar. Varsayılan değer denetimin türüne bağlıdır. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Denetimin Başlık özelliğini alır veya ayarlar. Varsayılan değer boş bir dizedir. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Hemen alt kontrollerin koleksiyonunu alır. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Geri Döndürür`doğru` eğer kontrol etkin durumdaysa. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Denetimin ön plan rengini alır veya ayarlar. Varsayılan değer, denetimin türüne bağlıdır. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Karşılıklı olarak birbirini dışlayan denetimlerden oluşan bir grubu belirten bir dize alır veya ayarlar. Varsayılan değer boş bir dizedir. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Kontrolün yüksekliğini noktalar halinde alır veya ayarlar. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Geri Döndürür`doğru` eğer kontrol bir`Forms2OleControl` . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | ActiveX denetiminin adını alır veya ayarlar. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Forms 2.0 denetiminin türünü alır. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Genellikle kontrol durumunu temsil eden temel Değer özelliğini alır. Örneğin işaretli seçenek düğmesi '1' değerine sahipken, işaretsiz düğme '0' değerine sahiptir. Varsayılan değer boş bir dizedir. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Kontrolün genişliğini noktalar halinde alır veya ayarlar. |

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

* class [OleControl](../olecontrol/)
* ad alanı [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../)
