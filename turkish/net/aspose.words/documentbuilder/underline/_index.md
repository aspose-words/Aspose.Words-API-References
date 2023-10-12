---
title: DocumentBuilder.Underline
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder mülk. Geçerli yazı tipinin alt çizgi türünü alır/ayarlar.
type: docs
weight: 190
url: /tr/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

Geçerli yazı tipinin alt çizgi türünü alır/ayarlar.

```csharp
public Underline Underline { get; set; }
```

### Örnekler

Belge oluşturucu tarafından eklenen metnin nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// Oluşturucu, biçimlendirmeyi mevcut paragrafına ve daha sonra eklediği yeni metne uygular.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### Ayrıca bakınız

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


