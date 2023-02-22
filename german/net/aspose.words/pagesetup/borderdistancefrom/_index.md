---
title: PageSetup.BorderDistanceFrom
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Ruft einen Wert ab oder legt einen Wert fest der angibt ob der angegebene Seitenrand vom Rand der Seite oder vom umgebenden Text gemessen wird.
type: docs
weight: 40
url: /de/net/aspose.words/pagesetup/borderdistancefrom/
---
## PageSetup.BorderDistanceFrom property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der angegebene Seitenrand vom Rand der Seite oder vom umgebenden Text gemessen wird.

```csharp
public PageBorderDistanceFrom BorderDistanceFrom { get; set; }
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

* enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


