---
title: DocumentBuilder.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words for .NET
description: DocumentBuilder Italic mülk. Yazı tipi italik olarak biçimlendirilmişse doğrudur C#'da.
type: docs
weight: 140
url: /tr/net/aspose.words/documentbuilder/italic/
---
## DocumentBuilder.Italic property

Yazı tipi italik olarak biçimlendirilmişse doğrudur.

```csharp
public bool Italic { get; set; }
```

## Örnekler

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
