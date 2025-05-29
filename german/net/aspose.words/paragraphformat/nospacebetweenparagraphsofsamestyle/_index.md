---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words für .NET
description: Entdecken Sie die ParagraphFormat-Eigenschaft „NoSpaceBetweenParagraphsOfSameStyle“. Optimieren Sie Ihr Dokumentlayout, indem Sie den Abstand zwischen Absätzen gleichen Stils verringern.
type: docs
weight: 250
url: /de/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

Wann`WAHR` ,[`SpaceBefore`](../spacebefore/) Und[`SpaceAfter`](../spaceafter/) wird zwischen den Absätzen desselben Stils ignoriert .

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## Bemerkungen

Diese Einstellung wird nur wirksam, wenn sie auf einen Absatzstil angewendet wird. Wenn sie direkt auf einen Absatz angewendet wird, hat sie keine Auswirkung.

## Beispiele

Zeigt, wie zwischen Absätzen mit demselben Stil kein Abstand hergestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenden Sie vor und nach den Absätzen, die dieser Builder erstellt, einen großen Abstand an.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Setzen Sie das Flag „NoSpaceBetweenParagraphsOfSameStyle“ auf „true“, um es anzuwenden
// kein Abstand zwischen Absätzen mit demselben Stil, wodurch ähnliche Absätze gruppiert werden.
// Lassen Sie das Flag „NoSpaceBetweenParagraphsOfSameStyle“ auf „false“
// um den Abstand auf jeden Absatz gleichmäßig anzuwenden.
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
