---
title: Enum ImlRenderingMode
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.ImlRenderingMode uppräkning. Anger hur bläckobjekt InkML renderas till fasta sidformat.
type: docs
weight: 5250
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
| Fallback | `0` | Om reservform är tillgänglig för ink (InkML)-objekt, återger Aspose.Words reservform istället för InkML. |
| InkML | `1` | Aspose.Words ignorerar fall-back form av ink (InkML) objekt och återger InkML själv. Detta är standardläget. |

### Exempel

Visar hur man renderar Ink-objekt.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Set 'ImlRenderingMode.InkML' ignorerar fall-back form av ink (InkML) objekt och renderar InkML själv.
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


