---
title: IDocumentProcessorPlugin.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words per .NET
description: Salva i documenti senza sforzo con il metodo di salvataggio IDocumentProcessorPlugin, assicurando un output ottimale con opzioni di salvataggio personalizzabili in base alle tue esigenze.
type: docs
weight: 30
url: /it/net/aspose.words/idocumentprocessorplugin/save/
---
## IDocumentProcessorPlugin.Save method

Salva il documento caricato da[`Load`](../load/) metodo al flusso di output utilizzando le opzioni di salvataggio specificate.

```csharp
public void Save(Stream outputStream, SaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputStream | Stream | Il flusso di output. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |

## Osservazioni

Se il formato di output specificato è immagine, solo l'immagine della prima pagina viene salvata nel flusso di output. Se il formato di salvataggio specificato non è supportato nativamente dal plugin (richiede il caricamento su[`Document`](../../document/)), il metodo genera un'eccezione.

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* interface [IDocumentProcessorPlugin](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
