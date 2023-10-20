---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: Aspose.Words per .NET
description: Font DoubleStrikeThrough proprietà. Vero se il carattere è formattato come testo barrato doppio in C#.
type: docs
weight: 90
url: /it/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

Vero se il carattere è formattato come testo barrato doppio.

```csharp
public bool DoubleStrikeThrough { get; set; }
```

## Esempi

Mostra come aggiungere una riga barrata al testo.

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
