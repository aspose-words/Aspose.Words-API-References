---
title: TextBoxControl Class
linktitle: TextBoxControl
articleTitle: TextBoxControl
second_title: .NET için Aspose.Words
description: Verilerden veya kullanıcı girdilerinden organize edilmiş metni zahmetsizce görüntülemek için Aspose.Words.Drawing.Ole.TextBoxControl sınıfını keşfedin. Belge yönetiminizi bugün geliştirin!
type: docs
weight: 1520
url: /tr/net/aspose.words.drawing.ole/textboxcontrol/
---
## TextBoxControl class

TextBox denetimi, düzenlenmiş bir veri kümesinden veya kullanıcı girdisinden metin görüntüler.

```csharp
public class TextBoxControl : MorphDataControl
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
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Geri Döndürür`doğru` eğer kontrol bir[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | ActiveX denetiminin adını alır veya ayarlar. |
| [Text](../../aspose.words.drawing.ole/textboxcontrol/text/) { get; set; } | Denetimin metnini alır veya ayarlar. |
| override [Type](../../aspose.words.drawing.ole/textboxcontrol/type/) { get; } | Forms 2.0 denetiminin türünü alır. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Genellikle kontrol durumunu temsil eden temel Değer özelliğini alır. Örneğin işaretli seçenek düğmesi '1' değerine sahipken, işaretsiz düğme '0' değerine sahiptir. Varsayılan değer boş bir dizedir. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Kontrolün genişliğini noktalar halinde alır veya ayarlar. |

## Örnekler

TextBox OLE denetiminin metninin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Ayrıca bakınız

* class [MorphDataControl](../morphdatacontrol/)
* ad alanı [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../)
