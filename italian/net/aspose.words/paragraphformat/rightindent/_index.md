---
title: ParagraphFormat.RightIndent
linktitle: RightIndent
articleTitle: RightIndent
second_title: Aspose.Words per .NET
description: Scopri come regolare facilmente il rientro corretto dei tuoi paragrafi con la proprietà ParagraphFormat RightIndent. Migliora la formattazione del tuo documento oggi stesso!
type: docs
weight: 280
url: /it/net/aspose.words/paragraphformat/rightindent/
---
## ParagraphFormat.RightIndent property

Ottiene o imposta il valore (in punti) che rappresenta il rientro corretto per il paragrafo.

```csharp
public double RightIndent { get; set; }
```

## Esempi

Mostra come configurare la formattazione del paragrafo per creare testo decentrato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Centra tutto il testo scritto dal generatore di documenti e imposta i rientri.
// La configurazione di rientro riportata di seguito creerà un corpo di testo che verrà posizionato in modo asimmetrico sulla pagina.
// Il "centro" rispetto al quale allineiamo il testo sarà la parte centrale del corpo del testo, non la parte centrale della pagina.
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
