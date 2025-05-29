---
title: OptionButtonControl Class
linktitle: OptionButtonControl
articleTitle: OptionButtonControl
second_title: .NET için Aspose.Words
description: Uygulamalarınızda özel seçim seçenekleri oluşturmak için mükemmel olan Aspose.Words.Drawing.Ole.OptionButtonControl sınıfını keşfedin. Kullanıcı deneyimini bugün geliştirin!
type: docs
weight: 1510
url: /tr/net/aspose.words.drawing.ole/optionbuttoncontrol/
---
## OptionButtonControl class

OptionButton denetimi, karşılıklı olarak birbirini dışlayan sınırlı sayıda seçenek arasından tek bir seçeneği etkinleştirir.

```csharp
public class OptionButtonControl : MorphDataControl
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
| [Selected](../../aspose.words.drawing.ole/optionbuttoncontrol/selected/) { get; set; } | Bu değeri belirten bir Boole değeri alır veya ayarlar`OptionButtonControl` seçilip seçilmediğini. |
| override [Type](../../aspose.words.drawing.ole/optionbuttoncontrol/type/) { get; } | Forms 2.0 denetiminin türünü alır. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Genellikle kontrol durumunu temsil eden temel Değer özelliğini alır. Örneğin işaretli seçenek düğmesi '1' değerine sahipken, işaretsiz düğme '0' değerine sahiptir. Varsayılan değer boş bir dizedir. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Kontrolün genişliğini noktalar halinde alır veya ayarlar. |

## Örnekler

Radyo düğmesinin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Seçili ilk öğeyi seçimi kaldır.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// İkinci seçeneği seç butonu.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### Ayrıca bakınız

* class [MorphDataControl](../morphdatacontrol/)
* ad alanı [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../)
