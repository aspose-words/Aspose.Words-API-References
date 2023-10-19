---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
linktitle: DocumentSplitHeadingLevel
articleTitle: DocumentSplitHeadingLevel
second_title: Aspose.Words for .NET
description: HtmlSaveOptions DocumentSplitHeadingLevel mülk. Belgenin bölüneceği maksimum başlık düzeyini belirtir. Varsayılan değer2  C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Belgenin bölüneceği maksimum başlık düzeyini belirtir. Varsayılan değer:`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

## Notlar

Ne zaman[`DocumentSplitCriteria`](../documentsplitcriteria/) içerirHeadingParagraph ve bu özellik 1'den 9'a kadar bir değere ayarlandığında, belge kullanılarak biçimlendirilmiş paragraflara bölünecektir.**Başlık 1** ,**Başlık 2** ,**Başlık 3**vb. stilleri belirtilen başlık seviyesine kadar.

Varsayılan olarak yalnızca**Başlık 1** Ve**Başlık 2** paragraflar belgenin bölünmesine neden olur. Bu özelliğin sıfıra ayarlanması, belgenin başlık paragraflarında hiç bölünmemesine neden olur.

## Örnekler

Bir çıktı HTML belgesinin başlıklara göre birkaç parçaya nasıl bölüneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Başlık" stilini kullanarak biçimlendirdiğimiz her paragraf başlık görevi görebilir.
// Her başlığın, başlık stili sayısına göre belirlenen bir başlık düzeyi de olabilir.
// Aşağıdaki başlıklar 1-3 arası seviyelere aittir.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// Bir HtmlSaveOptions nesnesi oluşturun ve bölme kriterlerini "HeadingParagraph" olarak ayarlayın.
// Bu kriterler, belgeyi "Başlık" stiline sahip paragraflardaki birkaç küçük belgeye böler,
// ve her belgeyi yerel dosya sisteminde ayrı bir HTML dosyasına kaydedin.
// Belgeyi 2'ye bölen maksimum başlık düzeyini de ayarlayacağız.
// Belgeyi kaydetmek onu 1. ve 2. düzey başlıklara böler, ancak 3 ila 9 arasında bölmez.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Dokümanımızın 1 - 2 arası düzeylerde dört başlığı var. Bu başlıklardan biri olmayacak
// belgenin başında olduğundan bir bölme noktası.
// Kaydetme işlemi belgemizi üç yerden dört küçük belgeye bölecek.
doc.Save(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html", options);

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html");

Assert.AreEqual("Heading #1", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-01.html");

Assert.AreEqual("Heading #2\r" +
                "Heading #3", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-02.html");

Assert.AreEqual("Heading #4", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-03.html");

Assert.AreEqual("Heading #5\r" +
                "Heading #6", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
