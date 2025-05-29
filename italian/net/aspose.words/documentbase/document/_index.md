---
title: DocumentBase.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words per .NET
description: Esplora le proprietà di DocumentBase per gestire in modo efficiente i tuoi documenti. Ottieni un accesso senza interruzioni e migliora il tuo flusso di lavoro oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words/documentbase/document/
---
## DocumentBase.Document property

Ottiene questa istanza.

```csharp
public override DocumentBase Document { get; }
```

## Esempi

Mostra come creare un documento semplice.

```csharp
Document doc = new Document();

// I nuovi oggetti Documento vengono forniti per impostazione predefinita con il set minimo di nodi
// necessario per iniziare ad aggiungere contenuti quali testo e forme: una sezione, un corpo e un paragrafo.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

### Guarda anche

* class [DocumentBase](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
