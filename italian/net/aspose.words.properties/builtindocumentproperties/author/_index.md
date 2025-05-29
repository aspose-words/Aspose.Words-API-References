---
title: BuiltInDocumentProperties.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words per .NET
description: Gestisci gli autori dei documenti senza sforzo con la proprietà Autore di BuiltInDocumentProperties. Imposta o recupera facilmente il nome dell'autore per una migliore organizzazione.
type: docs
weight: 10
url: /it/net/aspose.words.properties/builtindocumentproperties/author/
---
## BuiltInDocumentProperties.Author property

Ottiene o imposta il nome dell'autore del documento.

```csharp
public string Author { get; set; }
```

## Esempi

Mostra come lavorare con le proprietà del documento integrate nella categoria "Descrizione".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Di seguito sono riportate quattro proprietà predefinite del documento che dispongono di campi in grado di visualizzare i propri valori nel corpo del documento.
// 1 - Proprietà "Autore", che possiamo visualizzare utilizzando un campo AUTORE:
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - Proprietà "Titolo", che possiamo visualizzare utilizzando un campo TITLE:
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - Proprietà "Oggetto", che possiamo visualizzare utilizzando un campo SOGGETTO:
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - Proprietà "Commenti", che possiamo visualizzare utilizzando un campo COMMENTI:
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// La proprietà incorporata "Categoria" non ha un campo in grado di visualizzarne il valore.
properties.Category = "My category";

// Possiamo impostare più parole chiave per un documento separando il valore stringa della proprietà "Parole chiave" con punti e virgola.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// Possiamo fare clic con il pulsante destro del mouse su questo documento in Esplora risorse di Windows e trovare queste proprietà in "Proprietà" -> "Dettagli".
// La proprietà incorporata "Autore" si trova nel gruppo "Origine", mentre le altre si trovano nel gruppo "Descrizione".
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### Guarda anche

* class [BuiltInDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
