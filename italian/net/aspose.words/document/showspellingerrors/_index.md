---
title: Document.ShowSpellingErrors
linktitle: ShowSpellingErrors
articleTitle: ShowSpellingErrors
second_title: Aspose.Words per .NET
description: Controlla la visibilità degli errori ortografici nel tuo documento con la proprietà ShowSpellingErrors. Ottimizza il tuo processo di editing e migliora la qualità del documento.
type: docs
weight: 420
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
