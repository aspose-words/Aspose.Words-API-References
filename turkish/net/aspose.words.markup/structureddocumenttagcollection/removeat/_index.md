---
title: StructuredDocumentTagCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words for .NET
description: StructuredDocumentTagCollection RemoveAt yöntem. Belirtilen dizindeki yapılandırılmış belge etiketini kaldırır C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.markup/structureddocumenttagcollection/removeat/
---
## StructuredDocumentTagCollection.RemoveAt method

Belirtilen dizindeki yapılandırılmış belge etiketini kaldırır.

```csharp
public void RemoveAt(int index)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Koleksiyona bir dizin. |

## Örnekler

Yapılandırılmış belge etiketinin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

StructuredDocumentTagCollection structuredDocumentTags = doc.Range.StructuredDocumentTags;
IStructuredDocumentTag sdt;
for (int i = 0; i < structuredDocumentTags.Count; i++)
{
    sdt = structuredDocumentTags[i];
    Console.WriteLine(sdt.Title);
}

sdt = structuredDocumentTags.GetById(1691867797);
Assert.AreEqual(1691867797, sdt.Id);

Assert.AreEqual(5, structuredDocumentTags.Count);
// Yapılandırılmış belge etiketini kimliğe göre kaldırın.
structuredDocumentTags.Remove(1691867797);
// Yapılandırılmış belge etiketini 0 konumunda kaldırın.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Ayrıca bakınız

* class [StructuredDocumentTagCollection](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
