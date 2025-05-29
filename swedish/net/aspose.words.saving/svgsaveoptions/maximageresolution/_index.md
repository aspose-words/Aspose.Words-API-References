---
title: SvgSaveOptions.MaxImageResolution
linktitle: MaxImageResolution
articleTitle: MaxImageResolution
second_title: Aspose.Words för .NET
description: Kontrollera kvaliteten på dina exporterade rasterbilder med SvgSaveOptions MaxImageResolution. Ställ in pixeltätheten för optimala resultat. Standardvärde: 0.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/svgsaveoptions/maximageresolution/
---
## SvgSaveOptions.MaxImageResolution property

Hämtar eller ställer in ett värde i pixlar per tum som begränsar upplösningen för exporterade rasterbilder. Standardvärdet är noll.

```csharp
public int MaxImageResolution { get; set; }
```

## Anmärkningar

Om värdet för den här egenskapen inte är noll begränsar den upplösningen för exporterade rasterbilder. Det vill säga, bilder med högre upplösning samplas om ner till gränsen och bilder med lägre upplösning exporteras som de är.

Om värdet för den här egenskapen är noll exporteras alla rasterbilder utan omsampling.

## Exempel

Visar hur man ställer in en gräns för bildupplösning.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

### Se även

* class [SvgSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
