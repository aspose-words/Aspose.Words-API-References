---
title: PageSetup.BorderAppliesTo
linktitle: BorderAppliesTo
articleTitle: BorderAppliesTo
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „PageSetup BorderAppliesTo“ Ihr Dokumentlayout verbessert, indem sie den Druck der Seitenränder steuert und so für ein elegantes, professionelles Erscheinungsbild sorgt.
type: docs
weight: 30
url: /de/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

Gibt an, auf welchen Seiten der Seitenrand gedruckt wird.

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
```

## Beispiele

Zeigt, wie oben auf der ersten Seite ein breiter blauer Bandrand erstellt wird.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### Siehe auch

* enum [PageBorderAppliesTo](../../pageborderappliesto/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
