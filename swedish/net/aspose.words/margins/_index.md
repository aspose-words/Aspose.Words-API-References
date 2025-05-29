---
title: Margins Enum
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Margins-enum för anpassningsbara dokumentmarginaler. Förbättra din dokumentformatering med lättanvända förinställningar!
type: docs
weight: 4580
url: /sv/net/aspose.words/margins/
---
## Margins enumeration

Anger förinställda marginaler.

```csharp
public enum Margins
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Normal | `0` | Normala marginaler. |
| Narrow | `1` | Smala marginaler. |
| Moderate | `2` | Måttliga marginaler. |
| Wide | `3` | Breda marginaler. |
| Mirrored | `4` | Speglade marginaler. |
| Custom | `5` | Anpassade marginaler. |

## Exempel

Visar när dokumentets sidlayout ska beräknas om.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Att spara ett dokument till PDF, som en bild eller skriva ut för första gången kommer automatiskt
// cachelagrar dokumentets layout inom dess sidor.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Ändra dokumentet på något sätt.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// I den nuvarande versionen av Aspose.Words återskapas inte dokumentet automatiskt när du ändrar det
// den cachade sidlayouten. Om vi önskar den cachade layouten
// för att hålla oss uppdaterade måste vi uppdatera den manuellt.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
