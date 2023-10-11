---
title: StructuredDocumentTagCollection.GetById
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTagCollection yöntem. Yapılandırılmış belge etiketini tanımlayıcıya göre döndürür.
type: docs
weight: 30
url: /tr/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

Yapılandırılmış belge etiketini tanımlayıcıya göre döndürür.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| id | Int32 | Yapılandırılmış belge etiketi tanımlayıcısı. |

### Notlar

Belirtilen tanımlayıcıya sahip yapılandırılmış belge etiketi bulunamazsa null değerini döndürür.

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


