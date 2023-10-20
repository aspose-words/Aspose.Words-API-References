---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words für .NET
description: Aspose.Words.Layout.ContinuousSectionRestart opsomming. Stellt unterschiedliche Verhaltensweisen bei der Berechnung von Seitenzahlen in einem fortlaufenden Abschnitt dar der die Seitennummerierung neu startet in C#.
type: docs
weight: 3300
url: /de/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

Stellt unterschiedliche Verhaltensweisen bei der Berechnung von Seitenzahlen in einem fortlaufenden Abschnitt dar, der die Seitennummerierung neu startet.

```csharp
public enum ContinuousSectionRestart
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Always | `0` | Die Seitennummerierung beginnt unabhängig vom Inhaltsfluss immer neu. |
| FromNewPageOnly | `1` | Die Seitennummerierung beginnt nur dann neu, wenn vor dem Abschnitt auf der Seite, auf der der Abschnitt beginnt, kein anderer Inhalt vorhanden ist. |

## Beispiele

Zeigt, wie die Seitennummerierung in einem fortlaufenden Abschnitt gesteuert wird.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Standardmäßig entspricht das Verhalten von Aspose.Words dem von Microsoft Word 2019.
// Wenn Sie das alte Aspose.Words-Verhalten, repetitives Microsoft Word 2016, benötigen, verwenden Sie „ContinuousSectionRestart.FromNewPageOnly“.
// Die Seitennummerierung beginnt nur dann neu, wenn vor dem Abschnitt auf der Seite, auf der der Abschnitt beginnt, kein anderer Inhalt vorhanden ist.
// daher wird die Nummerierung ab der zweiten Seite auf 2 zurückgesetzt.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Siehe auch

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
