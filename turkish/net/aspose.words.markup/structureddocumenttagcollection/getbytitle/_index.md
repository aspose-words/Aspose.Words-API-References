---
title: StructuredDocumentTagCollection.GetByTitle
linktitle: GetByTitle
articleTitle: GetByTitle
second_title: .NET için Aspose.Words
description: Veri yönetimini kolaylaştırmak için başlığa göre ilk belge etiketini verimli bir şekilde alan StructuredDocumentTagCollection'daki GetByTitle yöntemini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

Belirtilen başlığa sahip koleksiyonda karşılaşılan ilk yapılandırılmış belge etiketini döndürür.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| title | String | Yapılandırılmış belge etiketinin başlığı. |

## Notlar

Belirtilen başlığa sahip yapılandırılmış belge etiketi bulunamazsa null döndürür.

## Örnekler

Yapılandırılmış belge etiketinin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Id'ye göre yapılandırılmış belge etiketini al.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Başlığa göre yapılandırılmış belge etiketini veya aralıklı etiketi alın.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Ayrıca bakınız

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
