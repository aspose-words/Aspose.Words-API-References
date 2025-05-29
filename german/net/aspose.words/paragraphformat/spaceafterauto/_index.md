---
title: ParagraphFormat.SpaceAfterAuto
linktitle: SpaceAfterAuto
articleTitle: SpaceAfterAuto
second_title: Aspose.Words für .NET
description: Entdecken Sie die ParagraphFormat-Eigenschaft „SpaceAfterAuto“. Passen Sie den Absatzabstand automatisch an, um ein übersichtlicheres, professionelleres Dokumentlayout zu erzielen.
type: docs
weight: 320
url: /de/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

Wahr, wenn der Abstand nach dem Absatz automatisch festgelegt wird.

```csharp
public bool SpaceAfterAuto { get; set; }
```

## Bemerkungen

Bei Einstellung auf`WAHR` überschreibt die Wirkung von[`SpaceAfter`](../spaceafter/).

Wenn Sie den Abstand davor und danach im Absatz auf „Automatisch“ einstellen, fügt Microsoft Word automatisch einen Abstand von 14 Punkten zwischen den Absätzen ein und zwar gemäß den folgenden Regeln:

* Normalerweise wird nach allen Absätzen ein Abstand hinzugefügt.
* In einer Aufzählungsliste oder nummerierten Liste wird ein Abstand nur nach dem letzten Element in der Liste hinzugefügt. Zwischen den Listenelementen wird kein Abstand hinzugefügt.
* In einer verschachtelten Aufzählungs- oder Nummerierungsliste wird kein Abstand hinzugefügt.
* Nach einer Tabelle wird normalerweise ein Abstand hinzugefügt.
* Nach einer Tabelle wird kein Abstand hinzugefügt, wenn es sich um den letzten Block in einer Tabellenzelle handelt.
* Nach dem letzten Absatz einer Tabellenzelle wird kein Abstand hinzugefügt.

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

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
