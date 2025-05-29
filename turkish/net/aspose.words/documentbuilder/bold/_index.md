---
title: DocumentBuilder.Bold
linktitle: Bold
articleTitle: Bold
second_title: .NET için Aspose.Words
description: DocumentBuilder Bold özelliğini keşfedin. Belgelerinizdeki metin görünürlüğünü ve etkisini artırmak için yazı tiplerini kolayca kalın olarak biçimlendirin. Tasarımınızı bugün güçlendirin!
type: docs
weight: 20
url: /tr/net/aspose.words/documentbuilder/bold/
---
## DocumentBuilder.Bold property

Yazı tipi kalın olarak biçimlendirilmişse doğrudur.

```csharp
public bool Bold { get; set; }
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
