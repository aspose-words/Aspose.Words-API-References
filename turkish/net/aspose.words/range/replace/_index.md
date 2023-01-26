---
title: Replace
second_title: Aspose.Words for .NET API Referansı
description: Belirtilen karakter dizesi modelinin tüm oluşumlarını bir yedek dizeyle değiştirir.
type: docs
weight: 80
url: /tr/net/aspose.words/range/replace/
---
## Replace(string, string) {#replace}

Belirtilen karakter dizesi modelinin tüm oluşumlarını bir yedek dizeyle değiştirir.

```csharp
public int Replace(string pattern, string replacement)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | String | Değiştirilecek bir dize. |
| replacement | String | Tüm kalıp oluşumlarını değiştirmek için bir dize. |

### Geri dönüş değeri

Yapılan değiştirme sayısı.

### Notlar

Kalıp normal ifade olarak kullanılmayacak. Lütfen kullanın`Replace` düzenli ifadelere ihtiyacınız varsa.

Kullanılan büyük/küçük harfe duyarsız karşılaştırma.

Yöntem, hem desen hem de değiştirme dizelerindeki sonları işleyebilir.

Molalarla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;p** - paragraf sonu
* **&amp;b** - Bölüm sonu
* **&amp;m** - sayfa sonu
* **&amp;l** - manuel satır sonu

Yöntemi kullan`Replace` daha esnek özelleştirmeye sahip olmak için.

### Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Numbers'dan sonra paragraf sonu ekler.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Bir belgenin içeriği üzerinde metin bul ve değiştir işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// Belgemizin içeriği üzerinde bir bul ve değiştir işlemi gerçekleştirin ve gerçekleşen değiştirme sayısını doğrulayın.
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
// bul ve değiştir işleminin bulduğu bir eşleşmeyi içeren.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Paragraf sonundan hemen önceki her noktayı bir ünlem işaretiyle değiştirin.
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

Normal bir ifadeyle belirtilen bir karakter deseninin tüm oluşumlarını başka bir dizeyle değiştirir.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | Regex | Eşleşmeleri bulmak için kullanılan bir normal ifade kalıbı. |
| replacement | String | Tüm kalıp oluşumlarını değiştirmek için bir dize. |

### Geri dönüş değeri

Yapılan değiştirme sayısı.

### Notlar

Normal ifade tarafından yakalanan tüm eşleşmeyi değiştirir.

Yöntem, hem desen hem de değiştirme dizelerindeki sonları işleyebilir.

Molalarla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;p** - paragraf sonu
* **&amp;b** - Bölüm sonu
* **&amp;m** - sayfa sonu
* **&amp;l** - manuel satır sonu

Yöntemi kullan`Replace` daha esnek özelleştirmeye sahip olmak için.

### Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Her sayıyı paragraf sonu ile değiştirir.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

Normal ifade deseninin tüm oluşumlarının başka metinlerle nasıl değiştirileceğini gösterir.

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

Belirtilen karakter dizesi modelinin tüm oluşumlarını bir yedek dizeyle değiştirir.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | String | Değiştirilecek bir dize. |
| replacement | String | Tüm kalıp oluşumlarını değiştirmek için bir dize. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) ek seçenekleri belirtmek için nesne. |

### Geri dönüş değeri

Yapılan değiştirme sayısı.

### Notlar

Kalıp normal ifade olarak kullanılmayacak. Lütfen kullanın`Replace` düzenli ifadelere ihtiyacınız varsa.

Yöntem, hem desen hem de değiştirme dizelerindeki sonları işleyebilir.

Molalarla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;p** - paragraf sonu
* **&amp;b** - Bölüm sonu
* **&amp;m** - sayfa sonu
* **&amp;l** - manuel satır sonu
* **&amp;&amp;** - &amp; karakter

### Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Numbers'dan sonra paragraf sonu ekler.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Belgenin alt bilgisindeki metnin nasıl değiştirileceğini gösterir.

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

// Değiştirilecek dizeleri bulurken büyük/küçük harf duyarlılığı uygulamak için "MatchCase" bayrağını "true" olarak ayarlayın.
// Değiştirilecek metni ararken büyük/küçük harf harflerini yok saymak için "MatchCase" bayrağını "false" olarak ayarlayın.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Yalnızca sözcükten oluşan bağımsız bul ve değiştir işlemlerinin nasıl değiştirileceğini gösterir.

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

Bir tablodaki ve hücredeki tüm String of text örneklerinin nasıl değiştirileceğini gösterir.

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

// Tüm tablo üzerinde bir bul ve değiştir işlemi gerçekleştir.
table.Range.Replace("Carrots", "Eggs", options);

// Tablonun son satırının son hücresinde bul ve değiştir işlemini gerçekleştirin.
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

Normal bir ifadeyle belirtilen bir karakter deseninin tüm oluşumlarını başka bir dizeyle değiştirir.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pattern | Regex | Eşleşmeleri bulmak için kullanılan bir normal ifade kalıbı. |
| replacement | String | Tüm kalıp oluşumlarını değiştirmek için bir dize. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) ek seçenekleri belirtmek için nesne. |

### Geri dönüş değeri

Yapılan değiştirme sayısı.

### Notlar

Normal ifade tarafından yakalanan tüm eşleşmeyi değiştirir.

Yöntem, hem desen hem de değiştirme dizelerindeki sonları işleyebilir.

Molalarla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **&amp;p** - paragraf sonu
* **&amp;b** - Bölüm sonu
* **&amp;m** - sayfa sonu
* **&amp;l** - manuel satır sonu
* **&amp;&amp;** - &amp; karakter

### Örnekler

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Her sayıyı paragraf sonu ile değiştirir.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

Tüm bu değiştirmeleri izlerken, bir normal ifade modelinin tüm oluşumlarının başka bir dizeyle nasıl değiştirileceğini gösterir.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();

    // "Değiştir" yönteminin yapacağı değişiklikleri izleyen bir geri arama ayarlayın.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Bul ve değiştir işlemiyle yapılan her metin değişikliğinin günlüğünü tutar
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

Bul ve değiştir işleminde bir eşleşmenin yerine tüm belgenin içeriğinin nasıl ekleneceğini gösterir.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Eşleşen metni içeren paragraftan sonra bir belge ekleyin.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Eşleşen metinle paragrafı kaldırın.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Bir paragraf veya tablodan sonra başka bir belgenin tüm düğümlerini ekler.
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
                // Bir bölümdeki son boş paragraf ise düğümü atlayın.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
