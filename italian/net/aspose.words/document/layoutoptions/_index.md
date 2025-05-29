---
title: Document.LayoutOptions
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words per .NET
description: Esplora la proprietà Document LayoutOptions per controllare efficacemente il layout del tuo documento. Sblocca opzioni di design flessibili per una presentazione ottimale.
type: docs
weight: 260
url: /it/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

Ottiene un[`LayoutOptions`](../../../aspose.words.layout/layoutoptions/) oggetto che rappresenta le opzioni per controllare il processo di layout di questo documento.

```csharp
public LayoutOptions LayoutOptions { get; }
```

## Esempi

Mostra come nascondere il testo in un documento di output renderizzato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Inserisce il testo nascosto, quindi specifica se desideriamo ometterlo dal documento renderizzato.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Mostra come visualizzare i segni di paragrafo in un documento di output renderizzato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Aggiungi alcuni paragrafi, quindi abilita i segni di paragrafo per mostrare la fine dei paragrafi
// con un simbolo pilcrow (¶) quando eseguiamo il rendering del documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una revisione, quindi cambia il colore di tutte le revisioni in verde.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Rimuovi la barra che appare a sinistra di ogni riga rivista.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Guarda anche

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
