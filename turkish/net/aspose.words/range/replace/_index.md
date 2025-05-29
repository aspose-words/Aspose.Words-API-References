---
title: Range.Replace
linktitle: Replace
articleTitle: Replace
second_title: .NET için Aspose.Words
description: Karakter dizisi deseninin tüm örneklerini Aralık Değiştirme yöntemiyle zahmetsizce değiştirin. Bu güçlü araçla metin işlemenizi geliştirin!
type: docs
weight: 100
url: /tr/net/aspose.words/range/replace/
---
## Replace(*string, string*) {#replace}

Belirtilen karakter dizisi deseninin tüm oluşumlarını bir değiştirme dizesiyle değiştirir.

```csharp
public int Replace(string pattern, string replacement)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | String | Değiştirilmesi gereken bir dize. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |

### Geri dönüş değeri

Yapılan yedek sayısı.

## Notlar

Desen normal ifade olarak kullanılmayacak. Lütfen kullanın`Replace` eğer düzenli ifadelere ihtiyacınız varsa.

Büyük/küçük harfe duyarlı olmayan karşılaştırma kullanıldı.

Metot hem desen hem de değiştirme dizelerindeki kopmaları işleyebilir.

Break'lerle çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;P** - paragraf sonu
* **&amp;B** - bölüm sonu
* **&amp;M** - sayfa sonu
* **&amp;l** - manuel satır sonu

Yöntemi kullan`Replace` daha esnek özelleştirmeye sahip olmak için.

## Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Sayılardan sonra paragraf sonu ekler.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Bir belgenin içeriğinde bul-ve-değiştir metin işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// Belgemizin içeriğinde bul-değiştir işlemini gerçekleştirelim ve gerçekleşen değiştirme sayısını doğrulayalım.
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
```

Bul ve değiştir işleminin eşleşme bulduğu paragraflara biçimlendirmenin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Her paragrafı sağa hizalamak için "Hizalama" özelliğini "ParagraphAlignment.Right" olarak ayarlayın
// bul ve değiştir işleminin bulduğu eşleşmeyi içeren.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Paragraf sonundan hemen önce gelen tüm noktaları ünlem işaretiyle değiştirin.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Range](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Replace(*Regex, string*) {#replace_2}

Bir düzenli ifade tarafından belirtilen bir karakter deseninin tüm oluşumlarını başka bir dizeyle değiştirir.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | Regex | Eşleşmeleri bulmak için kullanılan düzenli ifade deseni. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |

### Geri dönüş değeri

Yapılan yedek sayısı.

## Notlar

Düzenli ifade tarafından yakalanan tüm eşleşmeyi değiştirir.

Metot hem desen hem de değiştirme dizelerindeki kopmaları işleyebilir.

Break'lerle çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;P** - paragraf sonu
* **&amp;B** - bölüm sonu
* **&amp;M** - sayfa sonu
* **&amp;l** - manuel satır sonu

Yöntemi kullan`Replace` daha esnek özelleştirmeye sahip olmak için.

## Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Her sayıyı paragraf sonuyla değiştirir.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

Düzenli ifade deseninin tüm oluşumlarının başka metinle nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Range](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Replace(*string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

Belirtilen karakter dizisi deseninin tüm oluşumlarını bir değiştirme dizesiyle değiştirir.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | String | Değiştirilmesi gereken bir dize. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) ek seçenekleri belirtmek için nesne. |

### Geri dönüş değeri

Yapılan yedek sayısı.

## Notlar

Desen normal ifade olarak kullanılmayacak. Lütfen kullanın`Replace` eğer düzenli ifadelere ihtiyacınız varsa.

Metot hem desen hem de değiştirme dizelerindeki kopmaları işleyebilir.

Break'lerle çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;P** - paragraf sonu
* **&amp;B** - bölüm sonu
* **&amp;M** - sayfa sonu
* **&amp;l** - manuel satır sonu
* **&amp;&amp;** - &amp; karakter

## Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Sayılardan sonra paragraf sonu ekler.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Bir belgenin altbilgisindeki metnin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Bul ve değiştir işlemi gerçekleştirirken büyük/küçük harf duyarlılığının nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Değiştirilecek dizeleri bulurken büyük/küçük harf duyarlılığını uygulamak için "MatchCase" bayrağını "true" olarak ayarlayın.
// Değiştirilecek metni ararken karakter büyük/küçük harf ayrımını göz ardı etmek için "MatchCase" bayrağını "false" olarak ayarlayın.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Bağımsız kelime bazlı bul ve değiştir işlemlerinin nasıl açılıp kapatılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Bulunan metin başka bir kelimenin parçası değilse, onu değiştirmek için "FindWholeWordsOnly" bayrağını "true" olarak ayarlayın.
// Çevresindekilere bakılmaksızın tüm metni değiştirmek için "FindWholeWordsOnly" bayrağını "false" olarak ayarlayın.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

Bir tablo ve hücredeki tüm metin dizesi örneklerinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Carrots");
builder.InsertCell();
builder.Write("50");
builder.EndRow();
builder.InsertCell();
builder.Write("Potatoes");
builder.InsertCell();
builder.Write("50");
builder.EndTable();

FindReplaceOptions options = new FindReplaceOptions();
options.MatchCase = true;
options.FindWholeWordsOnly = true;

// Tüm tablo üzerinde bul ve değiştir işlemini gerçekleştir.
table.Range.Replace("Carrots", "Eggs", options);

// Tablonun son satırının son hücresinde bul-değiştir işlemini gerçekleştir.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Replace(*Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

Bir düzenli ifade tarafından belirtilen bir karakter deseninin tüm oluşumlarını başka bir dizeyle değiştirir.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | Regex | Eşleşmeleri bulmak için kullanılan düzenli ifade deseni. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) ek seçenekleri belirtmek için nesne. |

### Geri dönüş değeri

Yapılan yedek sayısı.

## Notlar

Düzenli ifade tarafından yakalanan tüm eşleşmeyi değiştirir.

Metot hem desen hem de değiştirme dizelerindeki kopmaları işleyebilir.

Break'lerle çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;P** - paragraf sonu
* **&amp;B** - bölüm sonu
* **&amp;M** - sayfa sonu
* **&amp;l** - manuel satır sonu
* **&amp;&amp;** - &amp; karakter

## Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Her sayıyı paragraf sonuyla değiştirir.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

Tüm değiştirmeleri izlerken, düzenli ifade deseninin tüm oluşumlarının başka bir dizeyle nasıl değiştirileceğini gösterir.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();

    // "Değiştir" yönteminin yapacağı tüm değişiklikleri izleyen bir geri çağırma ayarlayın.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Bir bul-değiştir işlemi tarafından yapılan her metin değişiminin günlüğünü tutar
/// ve orijinal eşleşen metnin değerini not eder.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

Bir bulma ve değiştirme işleminde bir eşleşmenin yerine tüm belgenin içeriğinin nasıl ekleneceğini gösterir.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

}

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Eşleşen metni içeren paragraftan sonra bir belge ekle.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Eşleşen metne sahip paragrafı kaldır.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Bir paragraf veya tablonun ardından başka bir belgenin tüm düğümlerini ekler.
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // Bir bölümdeki son boş paragraf ise düğümü atla.
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

### Ayrıca bakınız

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
