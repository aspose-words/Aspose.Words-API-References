---
title: IDocumentProcessorPlugin Interface
linktitle: IDocumentProcessorPlugin
articleTitle: IDocumentProcessorPlugin
second_title: Aspose.Words för .NET
description: Upptäck gränssnittet Aspose.Words IDocumentProcessorPlugin för att förbättra din dokumentbehandling med kraftfulla externa plugins för sömlös integration.
type: docs
weight: 3610
url: /sv/net/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface

Definierar ett gränssnitt för extern dokumentbehandlingsplugin.

```csharp
public interface IDocumentProcessorPlugin
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Append](../../aspose.words/idocumentprocessorplugin/append/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Lägg till dokumentet och läs det in med de angivna läsningsalternativen. |
| [Load](../../aspose.words/idocumentprocessorplugin/load/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Ladda dokumentet med de angivna laddningsalternativen. |
| [Save](../../aspose.words/idocumentprocessorplugin/save/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spara dokumentet som laddades av[`Load`](./load/) metoden till utdataströmmen med hjälp av de angivna sparalternativen. |
| [SetImageWatermark](../../aspose.words/idocumentprocessorplugin/setimagewatermark/)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Lägger till bildvattenmärke på varje sida i dokumentet som laddats av[`Load`](./load/) metod. |
| [SetTextWatermark](../../aspose.words/idocumentprocessorplugin/settextwatermark/)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Lägger till vattenstämpel på varje sida i dokumentet som laddats av[`Load`](./load/) metod. |
| [ToDocument](../../aspose.words/idocumentprocessorplugin/todocument/)() | Analyserar dokumentet som laddats av[`Load`](./load/) metod in i[`Document`](../document/) objekt. |
| [ToPages](../../aspose.words/idocumentprocessorplugin/topages/)(*[FixedPageSaveOptions](../../aspose.words.saving/fixedpagesaveoptions/)*) | Sparar varje sida i dokumentet som laddats av[`Load`](./load/) metod med de angivna alternativen för att spara fasta sidor. |

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
