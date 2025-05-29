---
title: StructuredDocumentTagCollection.GetById
linktitle: GetById
articleTitle: GetById
second_title: .NET için Aspose.Words
description: GetById yöntemiyle yapılandırılmış belge etiketlerini zahmetsizce alın. Verilerinize hızla erişin ve belge yönetimi verimliliğini artırın.
type: docs
weight: 30
url: /tr/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

Tanımlayıcıya göre yapılandırılmış belge etiketini döndürür.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| id | Int32 | Yapılandırılmış belge etiketi tanımlayıcısı. |

## Notlar

Belirtilen tanımlayıcıya sahip yapılandırılmış belge etiketi bulunamazsa null değerini döndürür.

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
