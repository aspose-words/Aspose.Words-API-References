---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words för .NET
description: Förnya dokumentets struktur med metoden UpdatePageLayout, vilket säkerställer en polerad och organiserad layout för förbättrad läsbarhet och presentation.
type: docs
weight: 830
url: /sv/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Återskapar dokumentets sidlayout.

```csharp
public void UpdatePageLayout()
```

## Anmärkningar

Den här metoden formaterar ett dokument till sidor och uppdaterar sidnummerrelaterade fält i dokumentet, såsom SIDA, SIDOR, SIDREF och REF. Den aktuella informationen om sidlayout krävs för en korrekt återgivning av dokumentet till fasta sidformat.

Den här metoden anropas automatiskt när du först konverterar ett dokument till PDF, XPS, bild eller skriver ut det. Om du däremot ändrar dokumentet efter rendering och sedan försöker rendera det igen kommer Aspose.Words inte att uppdatera sidlayouten automatiskt. I det här fallet bör du anropa`UpdatePageLayout` before rendering igen.

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

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
