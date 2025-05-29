---
title: Style.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words für .NET
description: Erfahren Sie, wie Sie die Stilprioritätseinstellungen verwalten, um die Stilsortierung in Ihrem Aufgabenbereich zu optimieren. Verbessern Sie Ihren Workflow mit effizienter Stilorganisation!
type: docs
weight: 160
url: /de/net/aspose.words/style/priority/
---
## Style.Priority property

Ruft den ganzzahligen Wert ab bzw. legt ihn fest, der die Priorität für die Sortierung der Stile im Aufgabenbereich „Stile“ darstellt.

```csharp
public int Priority { get; set; }
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
