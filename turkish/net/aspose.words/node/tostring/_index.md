---
title: Node.ToString
linktitle: ToString
articleTitle: ToString
second_title: .NET için Aspose.Words
description: Node ToString metodunu keşfedin, düğüm içeriğini gelişmiş veri işleme için özelleştirilebilir formatlarla dizelere zahmetsizce dönüştürün. Kodlamanızı bugün optimize edin!
type: docs
weight: 160
url: /tr/net/aspose.words/node/tostring/
---
## ToString(*[SaveFormat](../../saveformat/)*) {#tostring_1}

Düğümün içeriğini belirtilen biçimde bir dizeye aktarır.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Geri dönüş değeri

Belirtilen formattaki düğümün içeriği.

## Örnekler

Bir düğümde GetText ve ToString yöntemlerini çağırma arasındaki farkı gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText görünür metni, alan kodlarını ve özel karakterleri alacaktır.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString bize belgenin, geçilen bir kaydetme biçimine göre kaydedildiğinde nasıl görüneceğini verecektir.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

Bir düğümün içeriğini HTML formatında String'e aktarır.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// ToString metodunu html SaveFormat aşırı yüklemesini kullanarak çağırdığımızda,
// Düğümün içeriklerini ham html gösterimine dönüştürür.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Bu dönüşümün sonucunu SaveOptions nesnesini kullanarak da değiştirebiliriz.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

Liste öğeleri olan tüm paragrafların liste etiketlerinin nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Paragraf listesine sahip olup olmadığımızı bul. Belgemizde, listemiz düz Arap rakamlarını kullanır,
// üçte başlayıp altıda biten.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Bu düğümü metin formatına dönüştürdüğümüzde elde edeceğimiz metin budur.
     // Bu metin çıktısı liste etiketlerini atlayacaktır. Paragraf biçimlendirme karakterlerini kırpın.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Bu, listenin geçerli seviyesindeki paragrafın pozisyonunu alır. Birden fazla seviyeye sahip bir listemiz varsa,
    // bu bize o seviyedeki pozisyonunun ne olduğunu söyleyecektir.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Çıktıdaki metinle birlikte liste etiketini eklemek için bunları birleştirin.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## ToString(*[SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#tostring_2}

Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveOptions | SaveOptions | Düğümün nasıl kaydedileceğini denetleyen seçenekleri belirtir. |

### Geri dönüş değeri

Belirtilen formattaki düğümün içeriği.

## Örnekler

Bir düğümün içeriğini HTML formatında String'e aktarır.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// ToString metodunu html SaveFormat aşırı yüklemesini kullanarak çağırdığımızda,
// Düğümün içeriklerini ham html gösterimine dönüştürür.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Bu dönüşümün sonucunu SaveOptions nesnesini kullanarak da değiştirebiliriz.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
