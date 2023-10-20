---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words für .NET
description: ParagraphFormat NoSpaceBetweenParagraphsOfSameStyle eigendom. WannWAHR SpaceBefore UndSpaceAfter wird ignoriert zwischen den Absätzen desselben Stils in C#.
type: docs
weight: 240
url: /de/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

Wann`WAHR` ,[`SpaceBefore`](../spacebefore/) Und[`SpaceAfter`](../spaceafter/) wird ignoriert zwischen den Absätzen desselben Stils.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## Bemerkungen

Diese Einstellung wirkt sich nur aus, wenn sie auf einen Absatzstil angewendet wird. Wenn es direkt auf einen Absatz angewendet wird, hat es keine Auswirkung.

## Beispiele

Zeigt, wie man keinen Abstand zwischen Absätzen mit demselben Stil anwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Einen großen Abstand vor und nach den Absätzen anwenden, die dieser Builder erstellt.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Setzen Sie das Flag „NoSpaceBetweenParagraphsOfSameStyle“ auf „true“, um es anzuwenden
// Kein Abstand zwischen Absätzen mit demselben Stil, wodurch ähnliche Absätze gruppiert werden.
// Das Flag „NoSpaceBetweenParagraphsOfSameStyle“ auf „false“ belassen
// um jedem Absatz gleichmäßige Abstände zuzuweisen.
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

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
