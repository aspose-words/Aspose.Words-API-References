---
title: DocumentBuilder.Italic
linktitle: Italic
articleTitle: Italic
second_title: .NET için Aspose.Words
description: DocumentBuilder Italic özelliğini keşfedin. Belgelerinizde gelişmiş okunabilirlik ve stil için metninizi kolayca italik olarak biçimlendirin.
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

Bir posta birleştirme yerine bir belge oluşturucu kullanarak MERGEFIELD'ların verilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir posta birleştirme sırasında bir veri kaynağındaki aynı adlı sütunlardan veri kabul eden bazı MERGEFIELDS'leri ekleyin,
// ve sonra bunları elle doldurun.
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
