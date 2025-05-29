---
title: IDocumentProcessorPlugin Interface
linktitle: IDocumentProcessorPlugin
articleTitle: IDocumentProcessorPlugin
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words IDocumentProcessorPlugin-Schnittstelle, um Ihre Dokumentenverarbeitung mit leistungsstarken externen Plugins für eine nahtlose Integration zu verbessern.
type: docs
weight: 3610
url: /de/net/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface

Definiert eine Schnittstelle für ein externes Dokumentprozessor-Plugin.

```csharp
public interface IDocumentProcessorPlugin
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Append](../../aspose.words/idocumentprocessorplugin/append/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Hängen Sie das Dokument an und laden Sie es mit den angegebenen Ladeoptionen. |
| [Load](../../aspose.words/idocumentprocessorplugin/load/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Laden Sie das Dokument mit den angegebenen Ladeoptionen. |
| [Save](../../aspose.words/idocumentprocessorplugin/save/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Speichern Sie das geladene Dokument von[`Load`](./load/) Methode zum Ausgabestream unter Verwendung der angegebenen Speicheroptionen. |
| [SetImageWatermark](../../aspose.words/idocumentprocessorplugin/setimagewatermark/)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Fügt auf jeder Seite des Dokuments ein Bildwasserzeichen hinzu, das von[`Load`](./load/) Methode. |
| [SetTextWatermark](../../aspose.words/idocumentprocessorplugin/settextwatermark/)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Fügt Textwasserzeichen auf jeder Seite des Dokuments hinzu, das geladen wird von[`Load`](./load/) Methode. |
| [ToDocument](../../aspose.words/idocumentprocessorplugin/todocument/)() | Analysiert das Dokument, das geladen wurde von[`Load`](./load/) Methode in[`Document`](../document/) Objekt. |
| [ToPages](../../aspose.words/idocumentprocessorplugin/topages/)(*[FixedPageSaveOptions](../../aspose.words.saving/fixedpagesaveoptions/)*) | Speichert jede Seite des Dokuments, das geladen wurde von[`Load`](./load/) Methode unter Verwendung der angegebenen festen Seitenspeicheroptionen. |

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
