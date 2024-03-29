---
title: PageSetup.BorderDistanceFrom
linktitle: BorderDistanceFrom
articleTitle: BorderDistanceFrom
second_title: Aspose.Words für .NET
description: PageSetup BorderDistanceFrom eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob der angegebene Seitenrand vom Rand der Seite oder vom Text den er umgibt gemessen wird in C#.
type: docs
weight: 40
url: /de/net/aspose.words/pagesetup/borderdistancefrom/
---
## PageSetup.BorderDistanceFrom property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob der angegebene Seitenrand vom Rand der Seite oder vom Text, den er umgibt, gemessen wird.

```csharp
public PageBorderDistanceFrom BorderDistanceFrom { get; set; }
```

## Beispiele

Zeigt, wie man oben auf der ersten Seite einen breiten blauen Bandrand erstellt.

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

* enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
