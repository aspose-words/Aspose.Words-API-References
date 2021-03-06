---
title: ToString
second_title: Aspose.Words for .NET API Referansı
description: Düğümün içeriğini belirtilen biçimde bir dizeye aktarır.
type: docs
weight: 160
url: /tr/net/aspose.words/node/tostring/
---
## ToString(SaveFormat) {#tostring_1}

Düğümün içeriğini belirtilen biçimde bir dizeye aktarır.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Geri dönüş değeri

Düğümün içeriği belirtilen biçimde.

### Örnekler

Bir düğümde GetText ve ToString yöntemlerini çağırma arasındaki farkı gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText görünen metni, alan kodlarını ve özel karakterleri alacaktır.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString, geçmiş bir kaydetme biçimine kaydedilirse bize belgenin görünümünü verir.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Bir düğümün içeriğini HTML biçiminde Dize'ye aktarır.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// html SaveFormat aşırı yüklemesini kullanarak ToString yöntemini çağırdığımızda,
// düğümün içeriğini ham html temsillerine dönüştürür.
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

// Paragraf listesine sahip olup olmadığımızı bulun. Belgemizde listemizde düz Arapça sayılar kullanılıyor,
// üçte başlayan ve altıda biten.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Bu düğümü metin biçimine çıkardığımızda aldığımız metin budur.
    // Bu metin çıktısı liste etiketlerini atlayacak. Paragraf biçimlendirme karakterlerini kırpın. 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Bu, listenin geçerli düzeyinde paragrafın konumunu alır. Birden fazla seviye içeren bir listemiz varsa,
    // bu bize o seviyede hangi pozisyonda olduğunu söyleyecek.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Çıktıdaki metinle liste etiketini dahil etmek için bunları birleştirin.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../saveformat)
* class [Node](../../node)
* ad alanı [Aspose.Words](../../node)
* toplantı [Aspose.Words](../../../)

---

## ToString(SaveOptions) {#tostring_2}

Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveOptions | SaveOptions | Düğümün nasıl kaydedildiğini kontrol eden seçenekleri belirtir. |

### Geri dönüş değeri

Düğümün içeriği belirtilen biçimde.

### Örnekler

Bir düğümün içeriğini HTML biçiminde Dize'ye aktarır.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// html SaveFormat aşırı yüklemesini kullanarak ToString yöntemini çağırdığımızda,
// düğümün içeriğini ham html temsillerine dönüştürür.
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

* class [SaveOptions](../../../aspose.words.saving/saveoptions)
* class [Node](../../node)
* ad alanı [Aspose.Words](../../node)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
