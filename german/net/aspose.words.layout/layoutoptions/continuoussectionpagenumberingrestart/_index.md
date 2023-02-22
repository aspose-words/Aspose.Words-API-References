---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
second_title: Aspose.Words für .NET-API-Referenz
description: LayoutOptions eigendom. Ruft den Verhaltensmodus für die Berechnung von Seitenzahlen ab oder legt ihn fest wenn ein fortlaufender Abschnitt die Seitennummerierung neu startet.
type: docs
weight: 40
url: /de/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Ruft den Verhaltensmodus für die Berechnung von Seitenzahlen ab oder legt ihn fest, wenn ein fortlaufender Abschnitt die Seitennummerierung neu startet.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

### Bemerkungen

Der Standardwert istAlways . Es entspricht dem Verhalten von MS Word 2019, der zum Zeitpunkt der Einführung der Option die neueste Version war. Ältere Seitennummerierungslogik, die von MS Word 2016 demonstriert wurde, ist über diese Option verfügbar. Bitte[`ContinuousSectionRestart`](../../continuoussectionrestart/) für die Verhaltensbeschreibung.

### Beispiele

Zeigt, wie die Seitennummerierung in einem fortlaufenden Abschnitt gesteuert wird.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Standardmäßig entspricht das Verhalten von Aspose.Words dem von Microsoft Word 2019.
// Wenn Sie das alte Aspose.Words-Verhalten benötigen, sich wiederholendes Microsoft Word 2016, verwenden Sie 'ContinuousSectionRestart.FromNewPageOnly'.
// Die Seitennummerierung beginnt nur dann neu, wenn vor dem Abschnitt auf der Seite, auf der der Abschnitt beginnt, kein anderer Inhalt vorhanden ist.
// Aus diesem Grund wird die Nummerierung ab der zweiten Seite auf 2 zurückgesetzt.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Siehe auch

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../layoutoptions/)
* Montage [Aspose.Words](../../../)


