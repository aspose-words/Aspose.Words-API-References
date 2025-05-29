---
title: PageSetup.BorderAlwaysInFront
linktitle: BorderAlwaysInFront
articleTitle: BorderAlwaysInFront
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSetup-Eigenschaft BorderAlwaysInFront, um Seitenränder zu optimieren und so das Layout und die Sichtbarkeit sich überschneidender Texte und Objekte zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words/pagesetup/borderalwaysinfront/
---
## PageSetup.BorderAlwaysInFront property

Gibt an, wo der Seitenrand relativ zu sich überschneidenden Texten und Objekten positioniert wird.

```csharp
public bool BorderAlwaysInFront { get; set; }
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

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
