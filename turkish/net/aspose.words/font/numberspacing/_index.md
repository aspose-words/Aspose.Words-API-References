---
title: Font.NumberSpacing
linktitle: NumberSpacing
articleTitle: NumberSpacing
second_title: .NET için Aspose.Words
description: Gelişmiş okunabilirlik ve tasarım için rakam aralığını özelleştirmek üzere Font NumberSpacing özelliğini keşfedin. Tipografinizi bugün optimize edin!
type: docs
weight: 290
url: /tr/net/aspose.words/font/numberspacing/
---
## Font.NumberSpacing property

Görüntülenen rakamın aralık türünü alır veya ayarlar.

```csharp
public NumSpacing NumberSpacing { get; set; }
```

## Örnekler

Rakamların aralık türünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu efekt yalnızca MS Word'ün yeni sürümlerinde desteklenmektedir.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Ayrıca bakınız

* enum [NumSpacing](../../numspacing/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
