---
title: NodeImporter
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: .NET için Aspose.Words
description: NodeImporter oluşturucusunu keşfedin, veri yönetiminizi kolaylaştırmak ve proje verimliliğini artırmak için zahmetsizce yeni NodeImporter örnekleri oluşturun.
type: docs
weight: 10
url: /tr/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(*[DocumentBase](../../documentbase/), [DocumentBase](../../documentbase/), [ImportFormatMode](../../importformatmode/)*) {#constructor}

Yeni bir örneğini başlatır[`NodeImporter`](../) sınıf.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcDoc | DocumentBase | Kaynak belge. |
| dstDoc | DocumentBase | İçeri aktarılan düğümlerin sahibi olacak hedef belge. |
| importFormatMode | ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |

## Örnekler

Bir belgenin içeriğinin başka bir belgedeki yer imine nasıl ekleneceğini gösterir.

```csharp
public void InsertAtBookmark()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("InsertionPoint");
    builder.Write("We will insert a document here: ");
    builder.EndBookmark("InsertionPoint");

    Document docToInsert = new Document();
    builder = new DocumentBuilder(docToInsert);

    builder.Write("Hello world!");

    docToInsert.Save(ArtifactsDir + "NodeImporter.InsertAtMergeField.docx");

    Bookmark bookmark = doc.Range.Bookmarks["InsertionPoint"];
    InsertDocument(bookmark.BookmarkStart.ParentNode, docToInsert);

    Assert.AreEqual("We will insert a document here: " +
                    "\rHello world!", doc.GetText().Trim());
}

/// <summary>
/// Belirtilen düğümden sonra belgenin içeriğini ekler.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Bölümün gövdesindeki tüm blok düzeyindeki düğümler arasında döngü kur,
        // daha sonra bölümün son boş paragrafı olmayan her düğümü klonla ve ekle.
        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                destinationParent.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node should be either a paragraph or table.");
    }
}
```

### Ayrıca bakınız

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [NodeImporter](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## NodeImporter(*[DocumentBase](../../documentbase/), [DocumentBase](../../documentbase/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#constructor_1}

Yeni bir örneğini başlatır[`NodeImporter`](../) sınıf.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcDoc | DocumentBase | Kaynak belge. |
| dstDoc | DocumentBase | İçeri aktarılan düğümlerin sahibi olacak hedef belge. |
| importFormatMode | ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |
| importFormatOptions | ImportFormatOptions | İçeri aktarılan düğümü biçimlendirmek için çeşitli seçenekleri belirtir. |

## Örnekler

Aynı liste tanımlama tanımlayıcısına sahip listeleri içe aktarırken bir çakışmanın nasıl çözüleceğini gösterir.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Farklı bir liste tanımı kimliği uygulamak için "KeepSourceNumbering" özelliğini "true" olarak ayarlayın
// Aspose.Words ile aynı stilleri hedef belgelere aktarır.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Kaynak ve hedef belgelerdeki liste numaralandırma çakışmalarının nasıl çözüleceğini gösterir.

```csharp
// Özel liste numaralandırma şemasına sahip bir belge açın ve ardından onu kopyalayın.
// Her ikisinin de numaralandırma biçimi aynı olduğundan, bir belgeyi diğerine aktardığımızda biçimler çakışacaktır.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Belgenin klonunu orijinaline aktardığımızda ve sonra eklediğimizde,
// daha sonra aynı liste formatına sahip iki liste birleşecektir.
// "KeepSourceNumbering" bayrağını "false" olarak ayarlarsak, belge klonundan gelen liste
// orijinaline eklediğimiz her bir liste, onu eklediğimiz listenin numaralandırmasını sürdürecektir.
// Bu, iki listeyi etkili bir şekilde birleştirecektir.
// "KeepSourceNumbering" bayrağını "true" olarak ayarlarsak, belge klonu
 // liste orijinal numaralandırmasını koruyarak iki listenin ayrı listeler olarak görünmesini sağlar.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### Ayrıca bakınız

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [NodeImporter](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
