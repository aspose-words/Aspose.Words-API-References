---
title: Font.Superscript
linktitle: Superscript
articleTitle: Superscript
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font Apice e formatta facilmente il testo in apice per migliorare la leggibilità e lo stile dei tuoi documenti. Migliora il tuo design oggi stesso!
type: docs
weight: 450
url: /it/net/aspose.words/font/superscript/
---
## Font.Superscript property

Vero se il font è formattato come apice.

```csharp
public bool Superscript { get; set; }
```

## Esempi

Mostra come formattare il testo per spostarne la posizione.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Solleva questa sequenza di testo di 5 punti rispetto alla linea di base.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Abbassa questa sequenza di testo di 10 punti rispetto alla linea di base.
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
