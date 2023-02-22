---
title: RevisionCollection.AcceptAll
second_title: Aspose.Words for .NET API Referansı
description: RevisionCollection yöntem. Bu koleksiyondaki tüm düzeltmeleri kabul eder.
type: docs
weight: 40
url: /tr/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Bu koleksiyondaki tüm düzeltmeleri kabul eder.

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

// Belgeleri revizyonlarla karşılaştırmak bir istisna oluşturur.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Karşılaştırmadan sonra orijinal belge yeni bir revizyon kazanacak
// düzenlenen belgede farklı olan her öğe için.
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Bu revizyonları kabul etmek, orijinal belgeyi düzenlenmiş belgeye dönüştürecektir.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Ayrıca bakınız

* class [RevisionCollection](../)
* ad alanı [Aspose.Words](../../revisioncollection/)
* toplantı [Aspose.Words](../../../)


