---
title: StructuredDocumentTagCollection.GetById
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTagCollection metodo. Restituisce il tag del documento strutturato per identificatore.
type: docs
weight: 30
url: /it/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

Restituisce il tag del documento strutturato per identificatore.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| id | Int32 | L'identificatore del tag del documento strutturato. |

### Osservazioni

Restituisce null se non è possibile trovare il tag del documento strutturato con l'identificatore specificato.

### Esempi

Mostra come ottenere il tag del documento strutturato.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Ottieni il tag del documento strutturato in base all'ID.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// Ottieni il tag del documento strutturato o il tag con intervalli in base al titolo.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Guarda anche

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* assemblea [Aspose.Words](../../../)


