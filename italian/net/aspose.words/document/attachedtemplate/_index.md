---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words per .NET
description: Scopri come gestire in modo efficiente la proprietà Document AttachedTemplate. Imposta o recupera facilmente il percorso completo del modello del tuo documento per un'integrazione perfetta.
type: docs
weight: 20
url: /it/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Ottiene o imposta il percorso completo del modello allegato al documento.

```csharp
public string AttachedTemplate { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentNullException | Genera se si tenta di impostare su un`null` valore. |

## Osservazioni

Una stringa vuota indica che il documento è allegato al modello Normale.

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

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
