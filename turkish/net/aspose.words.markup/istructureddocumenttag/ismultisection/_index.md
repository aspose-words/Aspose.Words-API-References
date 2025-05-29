---
title: IStructuredDocumentTag.IsMultiSection
linktitle: IsMultiSection
articleTitle: IsMultiSection
second_title: .NET için Aspose.Words
description: Etiketinizin aralıklı çoklu bölüm olup olmadığını tanımlayan IStructuredDocumentTag'in IsMultiSection özelliğini keşfedin, bu sayede belge düzenlemesi ve işlevselliği artar.
type: docs
weight: 40
url: /tr/net/aspose.words.markup/istructureddocumenttag/ismultisection/
---
## IStructuredDocumentTag.IsMultiSection property

Bu örnek aralıklı (çok bölümlü) yapılandırılmış bir belge etiketi ise doğruyu döndürür.

```csharp
public bool IsMultiSection { get; }
```

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

* interface [IStructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
