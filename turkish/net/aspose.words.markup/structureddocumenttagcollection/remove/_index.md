---
title: StructuredDocumentTagCollection.Remove
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTagCollection yöntem. Belirtilen tanımlayıcıya sahip yapılandırılmış belge etiketini kaldırır.
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

### Örnekler

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
* ad alanı [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* toplantı [Aspose.Words](../../../)


