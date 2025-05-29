---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
linktitle: DocumentSplitHeadingLevel
articleTitle: DocumentSplitHeadingLevel
second_title: .NET için Aspose.Words
description: HtmlSaveOptions' DocumentSplitHeadingLevel ile belge bölmeyi optimize edin. Daha iyi organizasyon için başlık düzeylerini kontrol edin. Varsayılan olarak 2 olarak ayarlanmıştır.
type: docs
weight: 90
url: /tr/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Belgenin bölüneceği başlıkların maksimum düzeyini belirtir. Varsayılan değer`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

## Notlar

Ne zaman[`DocumentSplitCriteria`](../documentsplitcriteria/) içerirHeadingParagraph ve bu özellik 1 ile 9 arasında bir değere ayarlanırsa, belge kullanılarak biçimlendirilen paragraflara bölünecektir**Başlık 1** ,**Başlık 2** ,**Başlık 3**vb. belirtilen başlık düzeyine kadar stiller.

Varsayılan olarak yalnızca**Başlık 1** Ve**Başlık 2** paragraflar belgenin bölünmesine neden olur. Bu özelliği sıfıra ayarlamak, belgenin başlık paragraflarında hiç bölünmemesine neden olur.

## Örnekler

Çıktı HTML belgesinin başlıklara göre nasıl birkaç parçaya bölüneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Başlık" stilini kullanarak biçimlendirdiğimiz her paragraf başlık görevi görebilir.
// Her başlığın, başlık stilinin numarasına göre belirlenen bir başlık düzeyi de olabilir.
// Aşağıdaki başlıklar 1-3 seviyelerine aittir.
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

// Bir HtmlSaveOptions nesnesi oluşturun ve bölme ölçütünü "HeadingParagraph" olarak ayarlayın.
// Bu kriterler, "Başlık" stilleri olan paragraflardaki belgeyi birkaç küçük belgeye bölecektir.
// ve her belgeyi yerel dosya sisteminde ayrı bir HTML dosyasına kaydedin.
// Ayrıca belgeyi 2'ye bölen maksimum başlık seviyesini de ayarlayacağız.
// Belgeyi kaydetmek, onu 1. ve 2. düzey başlıklara bölecektir, ancak 3 ila 9. düzeylerde bölmeyecektir.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Belgemizin 1 - 2 seviyelerinde dört başlığı var. Bu başlıklardan biri olmayacak.
// Belgenin başında olduğu için bir bölünme noktası.
// Kaydetme işlemi belgemizi üç noktadan dört küçük belgeye bölecektir.
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
