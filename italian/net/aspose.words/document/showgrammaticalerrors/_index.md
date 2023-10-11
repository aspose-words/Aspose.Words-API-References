---
title: Document.ShowGrammaticalErrors
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Specifica se visualizzare gli errori grammaticali in questo documento.
type: docs
weight: 390
url: /it/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

Specifica se visualizzare gli errori grammaticali in questo documento.

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

### Esempi

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
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


