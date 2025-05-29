---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words per .NET
description: Scopri come utilizzare il metodo UnlinkFields per scollegare in modo efficiente i campi nell'intero documento, migliorando il flusso di lavoro di modifica.
type: docs
weight: 780
url: /it/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Scollega i campi nell'intero documento.

```csharp
public void UnlinkFields()
```

## Osservazioni

Sostituisce tutti i campi dell'intero documento con i risultati più recenti.

Per scollegare i campi in una parte specifica del documento utilizzare[`UnlinkFields`](../../range/unlinkfields/).

## Esempi

Mostra come scollegare tutti i campi nel documento.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
