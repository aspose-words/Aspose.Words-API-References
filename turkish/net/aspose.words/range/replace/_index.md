---
title: Range.Replace
second_title: Aspose.Words for .NET API Referansı
description: Range yöntem. Belirtilen karakter dizisi modelinin tüm oluşumlarını bir değiştirme dizesiyle değiştirir.
type: docs
weight: 90
url: /tr/net/aspose.words/range/replace/
---
## Replace(string, string) {#replace}

Belirtilen karakter dizisi modelinin tüm oluşumlarını bir değiştirme dizesiyle değiştirir.

```csharp
public int Replace(string pattern, string replacement)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | String | Değiştirilecek bir dize. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |

### Geri dönüş değeri

Yapılan değişiklik sayısı.

### Notlar

Desen normal ifade olarak kullanılmayacaktır. Lütfen kullanın`Replace`düzenli ifadelere ihtiyacınız varsa.

Büyük/küçük harfe duyarlı olmayan karşılaştırma kullanıldı.

Yöntem hem kalıp hem de değiştirme dizelerindeki kesintileri işleyebilir.

Molalarla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;P** - paragraf sonu
* **&amp;B** - Bölüm sonu
* **&amp;M** - sayfa sonu
* **&amp; ben** - manuel hat sonu

Yöntemi kullan`Replace` daha esnek özelleştirmeye sahip olmak için.

### Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Sayılardan sonra paragraf sonu ekler.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Bir belgenin içeriğinde metin bulma ve değiştirme işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// Belgemizin içeriği üzerinde bul ve değiştir işlemini gerçekleştirin ve gerçekleşen değişiklik sayısını doğrulayın.
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

// Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Her paragrafı sağa hizalamak için "Alignment" özelliğini "ParagraphAlignment.Right" olarak ayarlayın
// bulma ve değiştirme işleminin bulduğu eşleşmeyi içerir.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Paragraf sonundan hemen önceki her noktayı ünlem işaretiyle değiştirin.
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
* ad alanı [Aspose.Words](../../range/)
* toplantı [Aspose.Words](../../../)

---

## Replace(Regex, string) {#replace_2}

Normal bir ifadeyle belirtilen karakter modelinin tüm oluşumlarını başka bir dizeyle değiştirir.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | Regex | Eşleşmeleri bulmak için kullanılan normal ifade modeli. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |

### Geri dönüş değeri

Yapılan değişiklik sayısı.

### Notlar

Normal ifadenin yakaladığı eşleşmenin tamamını değiştirir.

Yöntem hem kalıp hem de değiştirme dizelerindeki kesintileri işleyebilir.

Molalarla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;P** - paragraf sonu
* **&amp;B** - Bölüm sonu
* **&amp;M** - sayfa sonu
* **&amp; ben** - manuel hat sonu

Yöntemi kullan`Replace` daha esnek özelleştirmeye sahip olmak için.

### Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Her sayıyı paragraf sonuyla değiştirir.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

Düzenli ifade modelinin tüm tekrarlarının başka metinle nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Range](../)
* ad alanı [Aspose.Words](../../range/)
* toplantı [Aspose.Words](../../../)

---

## Replace(string, string, FindReplaceOptions) {#replace_1}

Belirtilen karakter dizisi modelinin tüm oluşumlarını bir değiştirme dizesiyle değiştirir.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | String | Değiştirilecek bir dize. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Ek seçenekleri belirtmek için nesne. |

### Geri dönüş değeri

Yapılan değişiklik sayısı.

### Notlar

Desen normal ifade olarak kullanılmayacaktır. Lütfen kullanın`Replace`düzenli ifadelere ihtiyacınız varsa.

Yöntem hem kalıp hem de değiştirme dizelerindeki kesintileri işleyebilir.

Molalarla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;P** - paragraf sonu
* **&amp;B** - Bölüm sonu
* **&amp;M** - sayfa sonu
* **&amp; ben** - manuel hat sonu
* **&amp;&amp;** - &amp; karakter

### Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Sayılardan sonra paragraf sonu ekler.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Belgenin altbilgisindeki metnin nasıl değiştirileceğini gösterir.

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

// Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Değiştirilecek dizeleri bulurken büyük/küçük harf duyarlılığını uygulamak için "MatchCase" bayrağını "true" olarak ayarlayın.
// Değiştirilecek metni ararken karakter büyük/küçük harf durumunu dikkate almamak için "MatchCase" bayrağını "false" olarak ayarlayın.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Bağımsız salt sözcük bul ve değiştir işlemlerinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Bulunan metni başka bir kelimenin parçası değilse değiştirmek için "FindWholeWordsOnly" bayrağını "true" olarak ayarlayın.
// Çevresinden bağımsız olarak tüm metni değiştirmek için "FindWholeWordsOnly" bayrağını "false" olarak ayarlayın.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

Bir tablo ve hücredeki metin dizesinin tüm örneklerinin nasıl değiştirileceğini gösterir.

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

// Tablonun tamamında bulma ve değiştirme işlemini gerçekleştirin.
table.Range.Replace("Carrots", "Eggs", options);

// Tablonun son satırının son hücresinde bul ve değiştir işlemi gerçekleştir.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* ad alanı [Aspose.Words](../../range/)
* toplantı [Aspose.Words](../../../)

---

## Replace(Regex, string, FindReplaceOptions) {#replace_3}

Normal bir ifadeyle belirtilen karakter modelinin tüm oluşumlarını başka bir dizeyle değiştirir.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | Regex | Eşleşmeleri bulmak için kullanılan normal ifade modeli. |
| replacement | String | Desenin tüm oluşumlarını değiştirecek bir dize. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Ek seçenekleri belirtmek için nesne. |

### Geri dönüş değeri

Yapılan değişiklik sayısı.

### Notlar

Normal ifadenin yakaladığı eşleşmenin tamamını değiştirir.

Yöntem hem kalıp hem de değiştirme dizelerindeki kesintileri işleyebilir.

Molalarla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;P** - paragraf sonu
* **&amp;B** - Bölüm sonu
* **&amp;M** - sayfa sonu
* **&amp; ben** - manuel hat sonu
* **&amp;&amp;** - &amp; karakter

### Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Her sayıyı paragraf sonuyla değiştirir.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

Tüm bu değiştirmeleri izlerken, düzenli ifade modelinin tüm oluşumlarının başka bir dizeyle nasıl değiştirileceğini gösterir.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();

    // "Değiştir" yönteminin yapacağı değişiklikleri izleyen bir geri çağırma ayarlayın.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Bul ve değiştir işlemiyle gerçekleştirilen her metin değişiminin kaydını tutar
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

Bul ve değiştir işleminde bir eşleşmenin yerine belgenin içeriğinin tamamının nasıl ekleneceğini gösterir.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
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

        // Eşleşen metni içeren paragraftan sonra bir belge ekleyin.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Eşleşen metnin bulunduğu paragrafı kaldırın.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Başka bir belgenin tüm düğümlerini bir paragraf veya tablodan sonra ekler.
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
                // Bir bölümdeki son boş paragrafsa düğümü atla.
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
* ad alanı [Aspose.Words](../../range/)
* toplantı [Aspose.Words](../../../)


