---
title: Document.ShowGrammaticalErrors
linktitle: ShowGrammaticalErrors
articleTitle: ShowGrammaticalErrors
second_title: Aspose.Words per .NET
description: Controlla la visibilità degli errori grammaticali nel tuo documento con la proprietà ShowGrammaticalErrors. Migliora la chiarezza e la professionalità della scrittura senza sforzo.
type: docs
weight: 410
url: /it/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

Specifica se visualizzare gli errori grammaticali in questo documento.

```csharp
public bool ShowGrammaticalErrors { get; set; }
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

// Se queste opzioni sono abilitate, gli errori di ortografia saranno sottolineati
// nel documento di output da una linea rossa frastagliata, mentre una doppia linea blu evidenzierà gli errori grammaticali.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
