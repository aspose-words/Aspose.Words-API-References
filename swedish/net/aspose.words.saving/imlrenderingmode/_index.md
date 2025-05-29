---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words ImlRenderingMode-enum för optimal InkML-rendering. Förbättra dina dokumentutdata med exakt visualisering av bläckobjekt!
type: docs
weight: 6000
url: /sv/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Anger hur bläckobjekt (InkML) renderas till fasta sidformat.

```csharp
public enum ImlRenderingMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Fallback | `0` | Om en reservform är tillgänglig för ett bläckobjekt (InkML), renderar Aspose.Words reservformen istället för InkML. |
| InkML | `1` | Aspose.Words ignorerar alternativ form för InkML-objektet och renderar InkML självt. Detta är standardläget. |

## Exempel

Visar hur man renderar Ink-objekt.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Om 'ImlRenderingMode.InkML' sätts ignoreras alternativ form för Ink-objektet (InkML) och renderas InkML självt.
// Om renderingsresultatet är otillfredsställande,
// använd 'ImlRenderingMode.Fallback' för att få ett resultat som liknar tidigare versioner.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
