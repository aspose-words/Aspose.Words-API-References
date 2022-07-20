---
title: BorderAlwaysInFront
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt an wo der Seitenrand relativ zu sich überschneidenden Texten und Objekten positioniert wird.
type: docs
weight: 20
url: /de/net/aspose.words/pagesetup/borderalwaysinfront/
---
## PageSetup.BorderAlwaysInFront property

Gibt an, wo der Seitenrand relativ zu sich überschneidenden Texten und Objekten positioniert wird.

```csharp
public bool BorderAlwaysInFront { get; set; }
```

### Beispiele

Zeigt, wie Sie oben auf der ersten Seite einen breiten blauen Rahmen erstellen.

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

* class [PageSetup](../../pagesetup)
* namensraum [Aspose.Words](../../pagesetup)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->