---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words per .NET
description: Font StrikeThrough proprietà. Vero se il carattere è formattato come testo barrato in C#.
type: docs
weight: 390
url: /it/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

Vero se il carattere è formattato come testo barrato.

```csharp
public bool StrikeThrough { get; set; }
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
