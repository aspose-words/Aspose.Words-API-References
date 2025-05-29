---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Layout.ContinuousSectionRestart für flexible Seitennummerierungsoptionen in fortlaufenden Abschnitten. Verbessern Sie mühelos das Dokumentlayout!
type: docs
weight: 3750
url: /de/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

Stellt unterschiedliche Verhaltensweisen beim Berechnen von Seitenzahlen in einem fortlaufenden Abschnitt dar, der die Seitennummerierung neu startet.

```csharp
public enum ContinuousSectionRestart
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Always | `0` | Die Seitennummerierung wird unabhängig vom Inhaltsfluss immer neu gestartet. |
| FromNewPageOnly | `1` | Die Seitennummerierung wird nur dann neu gestartet, wenn sich vor dem Abschnitt auf der Seite, auf der der Abschnitt beginnt, kein anderer Inhalt befindet. |

## Beispiele

Zeigt, wie die Seitennummerierung in einem fortlaufenden Abschnitt gesteuert wird.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Standardmäßig entspricht das Verhalten von Aspose.Words dem von Microsoft Word 2019.
// Wenn Sie das alte Aspose.Words-Verhalten (wiederholtes Microsoft Word 2016) benötigen, verwenden Sie „ContinuousSectionRestart.FromNewPageOnly“.
// Die Seitennummerierung wird nur dann neu gestartet, wenn sich vor dem Abschnitt auf der Seite, auf der der Abschnitt beginnt, kein anderer Inhalt befindet.
// dadurch wird die Nummerierung ab der zweiten Seite auf 2 zurückgesetzt.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Siehe auch

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
