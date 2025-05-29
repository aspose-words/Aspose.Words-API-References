---
title: StructuredDocumentTagCollection.GetById
linktitle: GetById
articleTitle: GetById
second_title: Aspose.Words per .NET
description: Recupera facilmente i tag dei documenti strutturati con il metodo GetById. Accedi rapidamente ai tuoi dati e migliora l'efficienza della gestione dei documenti.
type: docs
weight: 30
url: /it/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

Restituisce il tag del documento strutturato in base all'identificatore.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| id | Int32 | Identificatore del tag del documento strutturato. |

## Osservazioni

Restituisce null se non è possibile trovare il tag del documento strutturato con l'identificatore specificato.

## Esempi

Mostra come ottenere il tag del documento strutturato.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Ottieni il tag del documento strutturato tramite Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Ottieni il tag del documento strutturato o il tag con intervallo in base al titolo.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Guarda anche

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
