---
title: Style.SemiHidden
linktitle: SemiHidden
articleTitle: SemiHidden
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SemiHidden-Eigenschaft die Sichtbarkeit von Stilen in der Stilgalerie und im Aufgabenbereich steuert und so Ihren Design-Workflow und Ihre Effizienz verbessert.
type: docs
weight: 170
url: /de/net/aspose.words/style/semihidden/
---
## Style.SemiHidden property

Ruft ab/legt fest, ob der Stil in der Stilgalerie und im Aufgabenbereich „Stile“ ausgeblendet wird.

```csharp
public bool SemiHidden { get; set; }
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
