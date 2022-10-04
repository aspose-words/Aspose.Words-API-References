---
title: Replacing
second_title: Aspose.Words for .NET API Referansı
description: Bir değiştirme yapılmadan hemen önce bulunan her eşleşme için değiştirme işlemi sırasında çağrılan kullanıcı tanımlı bir yöntem.
type: docs
weight: 10
url: /tr/net/aspose.words.replacing/ireplacingcallback/replacing/
---
## IReplacingCallback.Replacing method

Bir değiştirme yapılmadan hemen önce bulunan her eşleşme için değiştirme işlemi sırasında çağrılan kullanıcı tanımlı bir yöntem.

```csharp
public ReplaceAction Replacing(ReplacingArgs args)
```

### Geri dönüş değeri

A[`ReplaceAction`](../../replaceaction/) geçerli eşleşme için yapılacak eylemi belirten değer.

### Örnekler

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

* enum [ReplaceAction](../../replaceaction/)
* class [ReplacingArgs](../../replacingargs/)
* interface [IReplacingCallback](../)
* ad alanı [Aspose.Words.Replacing](../../ireplacingcallback/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
