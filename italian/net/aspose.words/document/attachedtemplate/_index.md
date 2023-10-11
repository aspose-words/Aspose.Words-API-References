---
title: Document.AttachedTemplate
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Ottiene o imposta il percorso completo del modello allegato al documento.
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
| ArgumentNullException | Genera se tenti di impostare su a`nullo` valore. |

### Osservazioni

Una stringa vuota significa che il documento è allegato al modello Normal.

### Esempi

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

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


