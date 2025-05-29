---
title: PageSetup.Margins
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words för .NET
description: Justera enkelt sidans marginaler med egenskapen PageSetup. Anpassa inställningarna för optimal layout och presentation. Förbättra ditt dokuments utseende!
type: docs
weight: 260
url: /sv/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

Returnerar eller ställer in förinställning[`Margins`](../../margins/) av sidan.

```csharp
public Margins Margins { get; set; }
```

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

* enum [Margins](../../margins/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
