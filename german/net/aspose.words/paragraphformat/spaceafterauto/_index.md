---
title: ParagraphFormat.SpaceAfterAuto
linktitle: SpaceAfterAuto
articleTitle: SpaceAfterAuto
second_title: Aspose.Words für .NET
description: ParagraphFormat SpaceAfterAuto eigendom. True wenn der Abstand nach dem Absatz automatisch festgelegt wird in C#.
type: docs
weight: 310
url: /de/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

True, wenn der Abstand nach dem Absatz automatisch festgelegt wird.

```csharp
public bool SpaceAfterAuto { get; set; }
```

## Bemerkungen

Wenn eingestellt auf`WAHR` , überschreibt die Wirkung von[`SpaceAfter`](../spaceafter/).

Wenn Sie „Abstand vor“ und „Abstand nach“ für Absätze auf „Automatisch“ setzen, fügt Microsoft Word automatisch einen Abstand von 14 Punkten zwischen den Absätzen hinzu gemäß den folgenden Regeln:

* Normalerweise wird der Abstand nach allen Absätzen hinzugefügt.
* In einer Liste mit Aufzählungszeichen oder Nummern wird der Abstand erst nach dem letzten Element in der Liste hinzugefügt. Zwischen den Listenelementen wird kein Abstand hinzugefügt.
* In einer verschachtelten Liste mit Aufzählungszeichen oder Nummern wird kein Abstand hinzugefügt.
* Der Abstand wird normalerweise nach einer Tabelle hinzugefügt.
* Nach einer Tabelle wird kein Abstand hinzugefügt, wenn es sich um den letzten Block in einer Tabellenzelle handelt.
* Nach dem letzten Absatz in einer Tabellenzelle wird kein Abstand hinzugefügt.

## Beispiele

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

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
