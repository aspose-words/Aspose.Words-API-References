---
title: DocumentBuilder.Italic
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder mülk. Yazı tipi italik olarak biçimlendirilmişse doğrudur.
type: docs
weight: 120
url: /tr/net/aspose.words/documentbuilder/italic/
---
## DocumentBuilder.Italic property

Yazı tipi italik olarak biçimlendirilmişse doğrudur.

```csharp
public bool Italic { get; set; }
```

### Örnekler

Adres mektup birleştirme yerine belge oluşturucu ile MERGEFIELD'lerin verilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres mektup birleştirme sırasında bir veri kaynağındaki aynı ada sahip sütunlardan veri kabul eden bazı MERGEFIELDS ekleyin,
// ve ardından bunları manuel olarak doldurun.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


