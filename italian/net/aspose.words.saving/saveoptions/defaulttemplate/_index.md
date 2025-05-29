---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words per .NET
description: Gestisci le tue opzioni di salvataggio con facilità! Imposta o ottieni il percorso e il nome file predefiniti del modello per un'elaborazione semplificata dei documenti. Ottimizza il tuo flusso di lavoro oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Ottiene o imposta il percorso al modello predefinito (incluso il nome del file). Il valore predefinito per questa proprietà è**stringa vuota** (Empty ).

```csharp
public string DefaultTemplate { get; set; }
```

## Osservazioni

Se specificato, questo percorso viene utilizzato per caricare il modello quando[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) È`VERO` , ma[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) è vuoto.

## Esempi

Mostra come impostare un modello predefinito per i documenti che non hanno modelli allegati.

```csharp
Document doc = new Document();

// Abilita l'aggiornamento automatico dello stile, ma non allegare un documento modello.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Poiché non esiste un documento modello, il documento non aveva alcun posto in cui tenere traccia delle modifiche di stile.
// Utilizzare un oggetto SaveOptions per impostare automaticamente un modello
// se un documento che stiamo salvando non ne ha uno.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
