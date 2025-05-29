---
title: IStructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words per .NET
description: Scopri la proprietà Titolo di IStructuredDocumentTag: definisci un nome intuitivo per il tuo SDT e migliora la chiarezza del documento. Scopri di più!
type: docs
weight: 140
url: /it/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Specifica il nome descrittivo associato a questo**SDT** . Non può essere nullo.

```csharp
public string Title { get; set; }
```

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

* interface [IStructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
