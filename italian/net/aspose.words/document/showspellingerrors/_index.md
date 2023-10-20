---
title: Document.ShowSpellingErrors
linktitle: ShowSpellingErrors
articleTitle: ShowSpellingErrors
second_title: Aspose.Words per .NET
description: Document ShowSpellingErrors proprietà. Specifica se visualizzare gli errori di ortografia in questo documento in C#.
type: docs
weight: 400
url: /it/net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

Specifica se visualizzare gli errori di ortografia in questo documento.

```csharp
public bool ShowSpellingErrors { get; set; }
```

## Esempi

Mostra come mostrare/nascondere gli errori nel documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci due frasi con errori che verrebbero rilevati
// dai correttori ortografici e grammaticali di Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Se queste opzioni sono abilitate, gli errori di ortografia verranno sottolineati
// nel documento di output da una linea rossa frastagliata e una doppia linea blu evidenzieranno gli errori grammaticali.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
