---
title: RevisionCollection.AcceptAll
second_title: Aspose.Words for .NET API Referansı
description: RevisionCollection yöntem. Bu koleksiyondaki tüm revizyonları kabul eder.
type: docs
weight: 40
url: /tr/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Bu koleksiyondaki tüm revizyonları kabul eder.

```csharp
public void AcceptAll()
```

### Örnekler

Belgelerin nasıl karşılaştırılacağını gösterir.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Dokümanların revizyonlarla karşılaştırılması bir istisna oluşturacaktır.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Karşılaştırma sonrasında orijinal doküman yeni bir revizyona kavuşacak
// düzenlenen belgedeki farklı olan her öğe için.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Bu revizyonların kabul edilmesi orijinal belgeyi düzenlenen belgeye dönüştürecektir.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Ayrıca bakınız

* class [RevisionCollection](../)
* ad alanı [Aspose.Words](../../revisioncollection/)
* toplantı [Aspose.Words](../../../)


