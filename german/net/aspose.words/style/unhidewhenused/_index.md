---
title: Style.UnhideWhenUsed
linktitle: UnhideWhenUsed
articleTitle: UnhideWhenUsed
second_title: Aspose.Words für .NET
description: Erfahren Sie, wie Sie die Eigenschaft „UnhideWhenUsed“ für Formatvorlagen verwalten. Steuern Sie die Sichtbarkeit in der Formatvorlagengalerie und im Aufgabenbereich, um das Design Ihres Dokuments zu verbessern.
type: docs
weight: 210
url: /de/net/aspose.words/style/unhidewhenused/
---
## Style.UnhideWhenUsed property

Ruft ab/legt fest, ob der im aktuellen Dokument verwendete Stil aus der Stilgalerie und dem Aufgabenbereich „Stile“ eingeblendet wird. „True“, wenn der verwendete Stil in der Stilgalerie angezeigt werden soll.

```csharp
public bool UnhideWhenUsed { get; set; }
```

## Beispiele

Zeigt, wie man einen Stil priorisiert und ausblendet.

```csharp
Document doc = new Document();
Style styleTitle = doc.Styles[StyleIdentifier.Subtitle];

if (styleTitle.Priority == 9)
    styleTitle.Priority = 10;

if (!styleTitle.UnhideWhenUsed)
    styleTitle.UnhideWhenUsed = true;

if (styleTitle.SemiHidden)
    styleTitle.SemiHidden = true;

doc.Save(ArtifactsDir + "Styles.StylePriority.docx");
```

### Siehe auch

* class [Style](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
