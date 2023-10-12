---
title: DocumentBuilder.Bold
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder mülk. Yazı tipi kalın olarak biçimlendirilmişse doğrudur.
type: docs
weight: 20
url: /tr/net/aspose.words/documentbuilder/bold/
---
## DocumentBuilder.Bold property

Yazı tipi kalın olarak biçimlendirilmişse doğrudur.

```csharp
public bool Bold { get; set; }
```

### Örnekler

Adres-mektup birleştirme yerine belge oluşturucuyla MERGEFIELD'lerin verilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres-mektup birleştirme sırasında veri kaynağındaki aynı isimdeki sütunlardan veri kabul eden bazı MERGEFIELDS'leri ekleyin,
// ve ardından manuel olarak doldurun.
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


