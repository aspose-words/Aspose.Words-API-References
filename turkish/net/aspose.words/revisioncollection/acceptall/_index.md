---
title: RevisionCollection.AcceptAll
linktitle: AcceptAll
articleTitle: AcceptAll
second_title: .NET için Aspose.Words
description: Tüm revizyonları sorunsuz bir şekilde entegre etmek, iş akışınızın verimliliğini ve iş birliğini artırmak için RevisionCollection AcceptAll yöntemini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Bu koleksiyondaki tüm revizyonları kabul eder.

```csharp
public void AcceptAll()
```

## Örnekler

Belgelerin nasıl karşılaştırılacağını gösterir.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Revizyonlu belgeleri karşılaştırmak bir istisna oluşturacaktır.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Karşılaştırmadan sonra orijinal belge yeni bir revizyon kazanacak
// düzenlenen belgede farklı olan her bir öğe için.
foreach (Revision r in docOriginal.Revisions)
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
