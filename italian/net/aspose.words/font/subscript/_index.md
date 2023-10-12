---
title: Font.Subscript
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Vero se il carattere è formattato come pedice.
type: docs
weight: 430
url: /it/net/aspose.words/font/subscript/
---
## Font.Subscript property

Vero se il carattere è formattato come pedice.

```csharp
public bool Subscript { get; set; }
```

### Esempi

Mostra come formattare il testo per spostarne la posizione.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Alza questa sequenza di testo 5 punti sopra la linea di base.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Abbassa questa sequenza di testo di 10 punti sotto la linea di base.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Aggiunge una sequenza di testo normale.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Aggiunge una sequenza di testo che appare come pedice.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Aggiunge una sequenza di testo che appare come apice.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


