---
title: PageBorderAppliesTo Enum
linktitle: PageBorderAppliesTo
articleTitle: PageBorderAppliesTo
second_title: Aspose.Words für .NET
description: Aspose.Words.PageBorderAppliesTo opsomming. Gibt an auf welchen Seiten der Seitenrand gedruckt wird in C#.
type: docs
weight: 4340
url: /de/net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

Gibt an, auf welchen Seiten der Seitenrand gedruckt wird.

```csharp
public enum PageBorderAppliesTo
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| AllPages | `0` | Der Seitenrand wird auf allen Seiten des Abschnitts angezeigt. |
| FirstPage | `1` | Der Seitenrand wird nur auf der ersten Seite des Abschnitts angezeigt. |
| OtherPages | `2` | Der Seitenrand wird auf allen Seiten außer der ersten Seite des Abschnitts angezeigt. |

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

* class [PageSetup](../pagesetup/)
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
