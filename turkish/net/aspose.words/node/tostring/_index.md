---
title: Node.ToString
second_title: Aspose.Words for .NET API Referansı
description: Node yöntem. Düğümün içeriğini belirtilen formatta bir dizeye aktarır.
type: docs
weight: 160
url: /tr/net/aspose.words/node/tostring/
---
## ToString(SaveFormat) {#tostring_1}

Düğümün içeriğini belirtilen formatta bir dizeye aktarır.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Geri dönüş değeri

Belirtilen formattaki düğümün içeriği.

### Örnekler

Bir düğümde GetText ve ToString yöntemlerinin çağrılması arasındaki farkı gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText görünür metni, alan kodlarını ve özel karakterleri de alacaktır.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString, eğer başarılı bir kaydetme biçiminde kaydedilirse, belgenin görünümünü bize verecektir.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Bir düğümün içeriğini HTML formatında String'e aktarır.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// ToString yöntemini html SaveFormat aşırı yüklemesini kullanarak çağırdığımızda,
// düğümün içeriğini ham html temsiline dönüştürür.
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

Liste öğesi olan tüm paragrafların liste etiketlerinin nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

//Paragraf listemizin olup olmadığını bulun. Belgemizde listemizde sade Arapça rakamlar kullanılıyor,
// üçte başlayıp altıda biten.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Bu düğümün çıktısını metin formatına aldığımızda elde ettiğimiz metin budur.
     // Bu metin çıktısı liste etiketlerini atlayacaktır. Paragraf biçimlendirme karakterlerini kırpın.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Bu, paragrafın listenin geçerli düzeyindeki konumunu alır. Birden fazla düzeyden oluşan bir listemiz varsa,
    // bu bize o seviyede hangi konumda olduğunu söyleyecektir.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Liste etiketini çıktıdaki metinle birlikte eklemek için bunları birleştirin.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* ad alanı [Aspose.Words](../../node/)
* toplantı [Aspose.Words](../../../)

---

## ToString(SaveOptions) {#tostring_2}

Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveOptions | SaveOptions | Düğümün nasıl kaydedileceğini kontrol eden seçenekleri belirtir. |

### Geri dönüş değeri

Belirtilen formattaki düğümün içeriği.

### Örnekler

Bir düğümün içeriğini HTML formatında String'e aktarır.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// ToString yöntemini html SaveFormat aşırı yüklemesini kullanarak çağırdığımızda,
// düğümün içeriğini ham html temsiline dönüştürür.
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
* ad alanı [Aspose.Words](../../node/)
* toplantı [Aspose.Words](../../../)


