---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font StrikeThrough. Formatta facilmente il testo barrato per dare maggiore risalto visivo ai tuoi progetti. Migliora la leggibilità oggi stesso!
type: docs
weight: 400
url: /it/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

Vero se il font è formattato come testo barrato.

```csharp
public bool StrikeThrough { get; set; }
```

## Esempi

Mostra come aggiungere una barratura al testo.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

Run run = new Run(doc, "Text with a single-line strikethrough.");
run.Font.StrikeThrough = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

run = new Run(doc, "Text with a double-line strikethrough.");
run.Font.DoubleStrikeThrough = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.StrikeThrough.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
