---
title: ParagraphFormat.SpaceBefore
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Ruft den Abstand in Punkten vor dem Absatz ab oder legt ihn fest.
type: docs
weight: 310
url: /de/net/aspose.words/paragraphformat/spacebefore/
---
## ParagraphFormat.SpaceBefore property

Ruft den Abstand (in Punkten) vor dem Absatz ab oder legt ihn fest.

```csharp
public double SpaceBefore { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn das Argument außerhalb des gültigen Wertebereichs lag. |

### Bemerkungen

Hat keine Auswirkung wann[`SpaceBeforeAuto`](../spacebeforeauto/) ist wahr.

Gültige Werte reichen von 0 bis einschließlich 1584.

### Beispiele

Zeigt, wie Sie den automatischen Absatzabstand festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Einen großen Abstand vor und nach Absätzen anwenden, die dieser Builder erstellt.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Setzen Sie diese Flags auf "true", um automatische Abstände anzuwenden,
// Ignoriert effektiv den Abstand in den Eigenschaften, die wir oben festgelegt haben.
// Lassen Sie sie auf "false", um unseren benutzerdefinierten Absatzabstand anzuwenden.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Fügen Sie zwei Absätze ein, die darüber und darunter einen Abstand haben, und speichern Sie das Dokument.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

Zeigt, wie kein Abstand zwischen Absätzen mit demselben Stil angewendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Einen großen Abstand vor und nach Absätzen anwenden, die dieser Builder erstellt.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Setzen Sie das Flag "NoSpaceBetweenParagraphsOfSameStyle" auf "true", um es anzuwenden
// kein Abstand zwischen Absätzen mit demselben Stil, wodurch ähnliche Absätze gruppiert werden.
// Lassen Sie das Flag "NoSpaceBetweenParagraphsOfSameStyle" auf "false"
// um gleichmäßige Abstände auf jeden Absatz anzuwenden.
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


