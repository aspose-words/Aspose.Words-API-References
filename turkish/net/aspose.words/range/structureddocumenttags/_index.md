---
title: Range.StructuredDocumentTags
linktitle: StructuredDocumentTags
articleTitle: StructuredDocumentTags
second_title: .NET için Aspose.Words
description: Belgenizin organizasyonunu ve işlevselliğini geliştiren kapsamlı bir yapılandırılmış belge etiketleri koleksiyonu sağlayan Range StructuredDocumentTags özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words/range/structureddocumenttags/
---
## Range.StructuredDocumentTags property

Bir`StructuredDocumentTags` . aralığındaki tüm yapılandırılmış belge etiketlerini temsil eden koleksiyon

```csharp
public StructuredDocumentTagCollection StructuredDocumentTags { get; }
```

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
// Id'ye göre yapılandırılmış belge etiketini kaldır.
structuredDocumentTags.Remove(1691867797);
// 0. konumdaki yapılandırılmış belge etiketini kaldırın.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Ayrıca bakınız

* class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* class [Range](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
