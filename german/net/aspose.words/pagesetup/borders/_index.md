---
title: PageSetup.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PageSetup Borders“, um einfach auf Ihre Seitenränder zuzugreifen und sie anzupassen, um Ihren Dokumenten ein elegantes, professionelles Aussehen zu verleihen.
type: docs
weight: 50
url: /de/net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

Ruft eine Sammlung der Seitenränder ab.

```csharp
public BorderCollection Borders { get; }
```

## Beispiele

Zeigt, wie man einen grünen, gewellten Seitenrand mit Schatten erstellt.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Siehe auch

* class [BorderCollection](../../bordercollection/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
