---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words per .NET
description: Scopri la proprietà NoSpaceBetweenParagraphsOfSameStyle di ParagraphFormat. Ottimizza il layout del tuo documento eliminando lo spazio tra paragrafi dello stesso stile.
type: docs
weight: 250
url: /it/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

Quando`VERO` ,[`SpaceBefore`](../spacebefore/) E[`SpaceAfter`](../spaceafter/) verrà ignorato tra i paragrafi dello stesso stile.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## Osservazioni

Questa impostazione ha effetto solo se applicata a uno stile di paragrafo. Se applicata direttamente a un paragrafo, non ha alcun effetto.

## Esempi

Mostra come non applicare alcuna spaziatura tra paragrafi con lo stesso stile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Applica una grande quantità di spaziatura prima e dopo i paragrafi che questo builder creerà.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Imposta il flag "NoSpaceBetweenParagraphsOfSameStyle" su "true" per applicare
// nessuna spaziatura tra paragrafi con lo stesso stile, che raggrupperà i paragrafi simili.
// Lascia il flag "NoSpaceBetweenParagraphsOfSameStyle" su "false"
// per applicare uniformemente la spaziatura a ogni paragrafo.
builder.ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle = noSpaceBetweenParagraphsOfSameStyle;

builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
