---
title: IDocumentProcessorPlugin Interface
linktitle: IDocumentProcessorPlugin
articleTitle: IDocumentProcessorPlugin
second_title: Aspose.Words per .NET
description: Scopri l'interfaccia Aspose.Words IDocumentProcessorPlugin per migliorare l'elaborazione dei tuoi documenti con potenti plugin esterni per un'integrazione perfetta.
type: docs
weight: 3610
url: /it/net/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface

Definisce un'interfaccia per il plugin dell'elaboratore di documenti esterno.

```csharp
public interface IDocumentProcessorPlugin
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Append](../../aspose.words/idocumentprocessorplugin/append/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Aggiungi il documento caricandolo con le opzioni di caricamento specificate. |
| [Load](../../aspose.words/idocumentprocessorplugin/load/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Carica il documento utilizzando le opzioni di caricamento specificate. |
| [Save](../../aspose.words/idocumentprocessorplugin/save/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Salva il documento caricato da[`Load`](./load/) metodo al flusso di output utilizzando le opzioni di salvataggio specificate. |
| [SetImageWatermark](../../aspose.words/idocumentprocessorplugin/setimagewatermark/)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Aggiunge una filigrana dell'immagine su ogni pagina del documento caricato da[`Load`](./load/) metodo. |
| [SetTextWatermark](../../aspose.words/idocumentprocessorplugin/settextwatermark/)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Aggiunge una filigrana di testo su ogni pagina del documento caricato da[`Load`](./load/) metodo. |
| [ToDocument](../../aspose.words/idocumentprocessorplugin/todocument/)() | Analizza il documento caricato da[`Load`](./load/) metodo in[`Document`](../document/) oggetto. |
| [ToPages](../../aspose.words/idocumentprocessorplugin/topages/)(*[FixedPageSaveOptions](../../aspose.words.saving/fixedpagesaveoptions/)*) | Salva ogni pagina del documento caricato da[`Load`](./load/) metodo che utilizza le opzioni di salvataggio della pagina fissa specificate. |

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
