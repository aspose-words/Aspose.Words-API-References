---
title: InsertHtml
second_title: Aspose.Words for .NET API Referansı
description: Belgeye bir HTML dizesi ekler.
type: docs
weight: 330
url: /tr/net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(string) {#inserthtml}

Belgeye bir HTML dizesi ekler.

```csharp
public void InsertHtml(string html)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| html | String | Belgeye eklenecek bir HTML dizesi. |

### Notlar

Bir HTML parçası veya tüm HTML belgesi eklemek için bu yöntemi kullanabilirsiniz.

### Örnekler

Bir belgeye html içeriği eklemek için bir belge oluşturucunun nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" + 
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" + 
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// HTML kodunun eklenmesi, her öğenin biçimlendirmesini eşdeğer belge metni biçimlendirmesine ayrıştırır.
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual("Paragraph right", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

Assert.AreEqual("Implicit paragraph left", paragraphs[1].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.True(paragraphs[1].Runs[0].Font.Bold);

Assert.AreEqual("Div center", paragraphs[2].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Center, paragraphs[2].ParagraphFormat.Alignment);

Assert.AreEqual("Heading 1 left.", paragraphs[3].GetText().Trim());
Assert.AreEqual("Heading 1", paragraphs[3].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtml.docx");
```

Birleştirme verilerini HTML belgeleri biçiminde işleyen özel bir geri aramayla adres mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// Adres mektup birleştirme, adı "html_" öneki ile başlayan bir MERGEFIELD ile karşılaşırsa,
/// bu geri arama, birleştirme verilerini HTML içeriği olarak ayrıştırır ve sonucu MERGEFIELD'in belge konumuna ekler.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Adres mektup birleştirme verileri bir MERGEFIELD ile birleştirdiğinde çağrılır.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Ayrıştırılmış HTML verilerini belgenin gövdesine ekleyin.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Birleştirilmiş içeriği zaten manuel olarak eklediğimiz için,
             // "Metin" özelliği aracılığıyla içerik döndürerek bu olaya yanıt vermemiz gerekmeyecek.
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Hiçbir şey yapma.
    }
}
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertHtml(string, bool) {#inserthtml_2}

Belgeye bir HTML dizesi ekler.

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| html | String | Belgeye eklenecek bir HTML dizesi. |
| useBuilderFormatting | Boolean | Biçimlendirmenin şurada belirtilmiş olup olmadığını gösteren bir değer.[`DocumentBuilder`](../) , HTML'den içe aktarılan metin için temel biçimlendirme olarak kullanılır. |

### Notlar

Bir HTML parçası veya tüm HTML belgesi eklemek için bu yöntemi kullanabilirsiniz.

Ne zaman*useBuilderFormatting* dır-dir`yanlış` , [`DocumentBuilder`](../) biçimlendirme yok sayılır ve eklenen text öğesinin biçimlendirmesi, varsayılan HTML biçimlendirmesine dayanır. Sonuç olarak, metin tarayıcılarda işlendiği gibi görünür.

Ne zaman*useBuilderFormatting* dır-dir`doğru` , eklenen metnin biçimlendirmesi,[`DocumentBuilder`](../) biçimlendirme, ve metin eklenmiş gibi görünüyor[`Write`](../write/) .

### Örnekler

HTML içeriği eklerken bir belge oluşturucu biçimlendirmesinin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Oluşturucu için bir metin hizalaması ayarlayın, belirtilen hizalamaya sahip ve olmayan bir HTML paragrafı ekleyin.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// İlk paragrafta belirtilen bir hizalama var. InsertHtml HTML kodunu ayrıştırdığında,
// HTML kodunda bulunan paragraf hizalama değeri her zaman belge oluşturucunun değerinin yerine geçer.
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

// İkinci paragrafta hizalama belirtilmemiş. Hizalama değeri doldurulabilir
// InsertHtml yöntemine ilettiğimiz bayrağa bağlı olarak oluşturucunun değerine göre.
Assert.AreEqual("Paragraph 2.", paragraphs[1].GetText().Trim());
Assert.AreEqual(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left,
    paragraphs[1].ParagraphFormat.Alignment);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertHtml(string, HtmlInsertOptions) {#inserthtml_1}

Belgeye bir HTML dizesi ekler. Ek seçenekleri belirlemeye izin verir.

```csharp
public void InsertHtml(string html, HtmlInsertOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| html | String | Belgeye eklenecek bir HTML dizesi. |
| options | HtmlInsertOptions | HTML dizesi eklendiğinde kullanılan seçenekler. |

### Notlar

Bir HTML parçası veya tüm HTML belgesi eklemek için bu yöntemi kullanabilirsiniz.

### Örnekler

Html eklerken seçeneklerin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// Varsayılan olarak "DocumentBuilder.InsertHtml", blok düzeyinde bir HTML öğesiyle biten bir HTML parçası ekler,
// normalde bu blok düzeyindeki öğeyi kapatır ve bir paragraf sonu ekler.
// Sonuç olarak, eklenen belgeden sonra yeni bir boş paragraf görünür.
// "HtmlInsertOptions.RemoveLastEmptyParagraph" belirtirsek, bu fazladan boş paragraflar kaldırılacaktır.
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### Ayrıca bakınız

* enum [HtmlInsertOptions](../../htmlinsertoptions/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
