---
title: ParagraphFormat.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words per .NET
description: ParagraphFormat LeftIndent proprietà. Ottiene o imposta il valore in punti che rappresenta il rientro sinistro del paragrafo in C#.
type: docs
weight: 180
url: /it/net/aspose.words/paragraphformat/leftindent/
---
## ParagraphFormat.LeftIndent property

Ottiene o imposta il valore (in punti) che rappresenta il rientro sinistro del paragrafo.

```csharp
public double LeftIndent { get; set; }
```

## Esempi

Mostra come configurare la formattazione del paragrafo per creare testo decentrato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Centra tutto il testo scritto dal generatore di documenti e imposta i rientri.
// La configurazione del rientro seguente creerà un corpo di testo che si posizionerà asimmetricamente sulla pagina.
// Il "centro" a cui allineiamo il testo sarà il centro del corpo del testo, non il centro della pagina.
ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.Alignment = ParagraphAlignment.Center;
paragraphFormat.LeftIndent = 100;
paragraphFormat.RightIndent = 50;
paragraphFormat.SpaceAfter = 25;

builder.Writeln(
    "This paragraph demonstrates how left and right indentation affects word wrapping.");
builder.Writeln(
    "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc.Save(ArtifactsDir + "DocumentBuilder.SetParagraphFormatting.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
