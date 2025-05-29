---
title: ParagraphFormat.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words für .NET
description: Steuern Sie den Absatzabstand mit der SpaceAfter-Eigenschaft. Passen Sie den Abstand in Punkten einfach an, um die Lesbarkeit und Präsentation Ihres Dokuments zu verbessern.
type: docs
weight: 310
url: /de/net/aspose.words/paragraphformat/spaceafter/
---
## ParagraphFormat.SpaceAfter property

Ruft den Abstand (in Punkten) nach dem Absatz ab oder legt ihn fest.

```csharp
public double SpaceAfter { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn das Argument außerhalb des Bereichs gültiger Werte liegt. |

## Bemerkungen

Hat keine Wirkung, wenn[`SpaceAfterAuto`](../spaceafterauto/) Ist`WAHR`.

Gültige Werte reichen von 0 bis einschließlich 1584.

## Beispiele

Zeigt, wie der automatische Absatzabstand eingestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenden Sie vor und nach den Absätzen, die dieser Builder erstellt, einen großen Abstand an.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Setzen Sie diese Flags auf „true“, um automatische Abstände anzuwenden,
// und ignoriert effektiv den Abstand in den Eigenschaften, die wir oben festgelegt haben.
// Wenn Sie sie auf „false“ belassen, wird unser benutzerdefinierter Absatzabstand angewendet.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Fügen Sie zwei Absätze ein, die oben und unten einen Abstand haben, und speichern Sie das Dokument.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

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
