---
title: Document.AutomaticallyUpdateStyles
linktitle: AutomaticallyUpdateStyles
articleTitle: AutomaticallyUpdateStyles
second_title: Aspose.Words per .NET
description: Scopri come la proprietà AutomaticallyUpdateStyles in MS Word garantisce la sincronizzazione degli stili del tuo documento con il modello ogni volta che lo apri, migliorando la coerenza.
type: docs
weight: 30
url: /it/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Ottiene o imposta un flag che indica se gli stili nel documento vengono aggiornati per corrispondere agli stili nel modello allegato ogni volta che il documento viene aperto in MS Word.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

## Esempi

Mostra come allegare un modello a un documento.

```csharp
Document doc = new Document();

// Per impostazione predefinita, i documenti Microsoft Word hanno un modello allegato denominato "Normal.dotm".
// Non esiste un modello predefinito per i documenti Aspose.Words vuoti.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Allega un modello, quindi imposta il flag per applicare le modifiche di stile
// all'interno del modello per applicare stili al nostro documento.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
