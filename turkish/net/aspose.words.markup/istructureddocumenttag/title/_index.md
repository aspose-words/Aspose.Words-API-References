---
title: IStructuredDocumentTag.Title
second_title: Aspose.Words for .NET API Referansı
description: IStructuredDocumentTag mülk. Bununla ilişkili kolay adı belirtir SDT . Boş olamaz.
type: docs
weight: 110
url: /tr/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Bununla ilişkili kolay adı belirtir **SDT** . Boş olamaz.

```csharp
public string Title { get; set; }
```

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

* interface [IStructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../istructureddocumenttag/)
* toplantı [Aspose.Words](../../../)


