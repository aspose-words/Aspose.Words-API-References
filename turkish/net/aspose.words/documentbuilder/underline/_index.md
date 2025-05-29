---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: .NET için Aspose.Words
description: Yazı tipi stillerini kolayca özelleştirmek için DocumentBuilder'ın Alt Çizgi özelliğini keşfedin. Profesyonel bir görünüm için çok yönlü alt çizgi seçenekleriyle belgelerinizi geliştirin.
type: docs
weight: 190
url: /tr/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

Geçerli yazı tipi için alt çizgi türünü alır/ayarlar.

```csharp
public Underline Underline { get; set; }
```

## Örnekler

Bir belge oluşturucu tarafından eklenen metnin nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// Oluşturucu biçimlendirmeyi geçerli paragrafına ve sonrasında eklediği yeni metne uygular.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### Ayrıca bakınız

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
