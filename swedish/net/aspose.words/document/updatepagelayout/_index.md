---
title: Document.UpdatePageLayout
second_title: Aspose.Words för .NET API Referens
description: Document metod. Bygger om dokumentets sidlayout.
type: docs
weight: 750
url: /sv/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Bygger om dokumentets sidlayout.

```csharp
public void UpdatePageLayout()
```

### Anmärkningar

Denna metod formaterar ett dokument till sidor och uppdaterar de sidnummerrelaterade fälten i dokumentet, t.ex. som PAGE, PAGES, PAGEREF och REF. Den uppdaterade sidlayoutinformationen krävs för en korrekt rendering av document till fasta sidformat.

Denna metod anropas automatiskt när du först konverterar ett dokument till PDF, XPS, bild eller skriver ut det. Men om du ändrar dokumentet efter renderingen och sedan försöker rendera det igen - kommer Aspose.Words inte att uppdatera sidlayouten automatiskt. I det här fallet bör du ringa`UpdatePageLayout` före rendering igen.

### Exempel

Visar när sidlayouten för dokumentet ska beräknas om.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Att spara ett dokument till PDF, till en bild eller skriva ut för första gången kommer automatiskt
// cachelagrar dokumentets layout på dess sidor.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Ändra dokumentet på något sätt.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;

  // I den nuvarande versionen av Aspose.Words återuppbyggs inte ändring av dokumentet automatiskt
// den cachade sidlayouten. Om vi önskar den cachade layouten
// för att hålla oss uppdaterade måste vi uppdatera den manuellt.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


