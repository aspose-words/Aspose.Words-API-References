---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: Aspose.Words per .NET
description: Scopri la proprietà Field DisplayResult che fornisce il testo per i risultati dei campi visualizzati, migliorando la chiarezza e l'esperienza utente.
type: docs
weight: 10
url: /it/net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

Ottiene il testo che rappresenta il risultato del campo visualizzato.

```csharp
public string DisplayResult { get; }
```

## Osservazioni

Il[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) il metodo deve essere chiamato per ottenere il valore corretto per the [`FieldListNum`](../../fieldlistnum/) ,[`FieldAutoNum`](../../fieldautonum/) ,[`FieldAutoNumOut`](../../fieldautonumout/) E[`FieldAutoNumLgl`](../../fieldautonumlgl/) campi.

## Esempi

Mostra come ottenere il testo effettivo visualizzato da un campo nel documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// Possiamo usare la proprietà DisplayResult per verificare quale testo esatto
// un campo verrebbe visualizzato al suo posto nel documento.
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

 // I campi non mantengono valori di risultato accurati in tempo reale.
// Per garantire che i nostri campi visualizzino risultati accurati in ogni momento,
// ad esempio subito prima di un'operazione di salvataggio, dobbiamo aggiornarli manualmente.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### Guarda anche

* class [Field](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
