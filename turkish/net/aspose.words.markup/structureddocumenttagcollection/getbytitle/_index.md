---
title: StructuredDocumentTagCollection.GetByTitle
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTagCollection yöntem. Koleksiyonda karşılaşılan ve belirtilen başlıktaki ilk yapılandırılmış belge etiketini döndürür.
type: docs
weight: 50
url: /tr/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

Koleksiyonda karşılaşılan ve belirtilen başlıktaki ilk yapılandırılmış belge etiketini döndürür.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| title | String | Yapılandırılmış belge etiketinin başlığı. |

### Notlar

Belirtilen başlığa sahip yapılandırılmış belge etiketi bulunamazsa null değerini döndürür.

### Örnekler

Yapılandırılmış belge etiketinin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Yapılandırılmış belge etiketini kimliğe göre alın.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// Başlığa göre yapılandırılmış belge etiketini veya aralıklı etiketi alın.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Ayrıca bakınız

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* ad alanı [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* toplantı [Aspose.Words](../../../)


