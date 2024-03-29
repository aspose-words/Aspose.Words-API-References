---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words per .NET
description: SaveOptions DefaultTemplate proprietà. Ottiene o imposta il percorso del modello predefinito incluso il nome file. Il valore predefinito per questa proprietà èstringa vuota Empty in C#.
type: docs
weight: 40
url: /it/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è**stringa vuota** (Empty).

```csharp
public string DefaultTemplate { get; set; }
```

## Osservazioni

Se specificato, questo percorso viene utilizzato per caricare il modello quando[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) È`VERO` , ma[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) è vuoto.

## Esempi

Mostra come impostare un modello predefinito per i documenti a cui non sono allegati modelli.

```csharp
Document doc = new Document();

// Abilita l'aggiornamento automatico dello stile, ma non allega un documento modello.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Poiché non esiste un documento modello, il documento non aveva un posto dove tenere traccia delle modifiche di stile.
// Utilizza un oggetto SaveOptions per impostare automaticamente un modello
// se un documento che stiamo salvando non ne ha uno.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
