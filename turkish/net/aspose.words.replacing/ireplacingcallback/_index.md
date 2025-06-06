---
title: IReplacingCallback Interface
linktitle: IReplacingCallback
articleTitle: IReplacingCallback
second_title: .NET için Aspose.Words
description: Aspose.Words' IReplacingCallback arayüzüyle belge işlemenizi geliştirin. Kişiye özel sonuçlar için özel bul ve değiştir yöntemleri oluşturun.
type: docs
weight: 5360
url: /tr/net/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface

Bir bul ve değiştir işlemi sırasında kendi özel yönteminizin çağrılmasını istiyorsanız bu arayüzü uygulayın.

```csharp
public interface IReplacingCallback
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Replacing](../../aspose.words.replacing/ireplacingcallback/replacing/)(*[ReplacingArgs](../replacingargs/)*) | Bir değiştirme yapılmadan hemen önce bulunan her eşleşme için bir değiştirme işlemi sırasında çağrılan kullanıcı tanımlı bir yöntem. |

## Örnekler

Bir metin değiştirme işleminin düğümleri hangi sırayla geçtiğinin nasıl izleneceğini gösterir.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // İlk sayfa için farklı bir üstbilgi/altbilgi kullanılması arama sırasını etkileyecektir.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// Bir bul-değiştir işlemi sırasında, işlemin 'bulduğu' metni içeren her düğümün içeriğini kaydeder,
/// değiştirme gerçekleşmeden önceki hali.
/// Bu, metin değiştirme işleminin düğümleri hangi sırayla dolaşacağını görüntüler.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
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

* ad alanı [Aspose.Words.Replacing](../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../)
