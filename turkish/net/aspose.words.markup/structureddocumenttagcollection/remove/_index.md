---
title: StructuredDocumentTagCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: .NET için Aspose.Words
description: Düzgünleştirilmiş belge yönetimi için StructuredDocumentTagCollection Remove yöntemini kullanarak belirli yapılandırılmış belge etiketlerini zahmetsizce kaldırın.
type: docs
weight: 70
url: /tr/net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

Belirtilen tanımlayıcıya sahip yapılandırılmış belge etiketini kaldırır.

```csharp
public void Remove(int id)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| id | Int32 | Yapılandırılmış belge etiketi tanımlayıcısı. |

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

* class [StructuredDocumentTagCollection](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
