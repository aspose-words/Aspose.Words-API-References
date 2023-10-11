---
title: Document.LayoutOptions
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Ottiene aLayoutOptions oggetto che rappresenta le opzioni per controllare il processo di layout di questo documento.
type: docs
weight: 250
url: /it/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

Ottiene a[`LayoutOptions`](../../../aspose.words.layout/layoutoptions/) oggetto che rappresenta le opzioni per controllare il processo di layout di questo documento.

```csharp
public LayoutOptions LayoutOptions { get; }
```

### Esempi

Mostra come nascondere il testo in un documento di output sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Inserisci il testo nascosto, quindi specifica se desideriamo ometterlo da un documento renderizzato.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Mostra come visualizzare i segni di paragrafo in un documento di output sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Aggiungi alcuni paragrafi, quindi abilita i segni di paragrafo per mostrare la fine dei paragrafi
// con il simbolo pilcrow (¶) quando eseguiamo il rendering del documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Mostra come modificare l'aspetto delle revisioni in un documento di output sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una revisione, quindi cambia il colore di tutte le revisioni in verde.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Rimuove la barra che appare a sinistra di ogni riga modificata.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Guarda anche

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


