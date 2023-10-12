---
title: ParagraphFormat.SpaceBefore
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Ruft den Abstand in Punkt vor dem Absatz ab oder legt diesen fest.
type: docs
weight: 320
url: /de/net/aspose.words/paragraphformat/spacebefore/
---
## ParagraphFormat.SpaceBefore property

Ruft den Abstand (in Punkt) vor dem Absatz ab oder legt diesen fest.

```csharp
public double SpaceBefore { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn das Argument außerhalb des gültigen Wertebereichs lag. |

### Bemerkungen

Hat keine Auswirkung, wenn[`SpaceBeforeAuto`](../spacebeforeauto/) Ist`WAHR`.

Gültige Werte reichen von 0 bis einschließlich 1584.

### Beispiele

Zeigt, wie der automatische Absatzabstand eingestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Einen großen Abstand vor und nach den Absätzen anwenden, die dieser Builder erstellt.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Setzen Sie diese Flags auf „true“, um den automatischen Abstand anzuwenden.
// Der Abstand in den oben festgelegten Eigenschaften wird effektiv ignoriert.
// Wenn Sie sie auf „false“ belassen, wird unser benutzerdefinierter Absatzabstand angewendet.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Fügen Sie zwei Absätze mit Abstand darüber und darunter ein und speichern Sie das Dokument.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

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
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


