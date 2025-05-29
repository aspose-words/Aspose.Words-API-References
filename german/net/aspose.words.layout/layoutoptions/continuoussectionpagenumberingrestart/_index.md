---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
articleTitle: ContinuousSectionPageNumberingRestart
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „LayoutOptions ContinuousSectionPageNumberingRestart“ für eine nahtlose Steuerung der Seitennummerierung in fortlaufenden Abschnitten. Optimieren Sie noch heute Ihr Dokumentlayout!
type: docs
weight: 40
url: /de/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Ruft das Verhalten für die Berechnung der Seitenzahlen ab oder legt es fest, wenn ein fortlaufender Abschnitt die Seitennummerierung neu startet.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## Bemerkungen

Der Standardwert istAlways . Es entspricht dem Verhalten von MS Word 2019, der neuesten Version zum Zeitpunkt der Einführung der Option. Über diese Option ist eine ältere Seitennummerierungslogik von MS Word 2016 verfügbar. Bitte[`ContinuousSectionRestart`](../../continuoussectionrestart/) für die Verhaltensbeschreibung.

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

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
