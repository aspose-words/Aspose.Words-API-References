---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words för .NET
description: Optimera EMF-sparandet med ImageSaveOptions. Kontrollera GDI- eller Aspose.Words-rendererinställningarna för förbättrad bildkvalitet och prestanda.
type: docs
weight: 190
url: /sv/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

Hämtar eller anger ett värde som avgör om GDI+ eller Aspose.Words metafilrenderare ska användas vid sparning till EMF.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## Anmärkningar

Om inställd på`sann` GDI+ metafilrenderare används. Dvs. innehållet skrivs till GDI+ graphics -objektet och sparas i metafilen.

Om inställd på`falsk` Aspose.Words metafilrenderare används. Dvs. innehållet skrivs direkt till metafilformatet med Aspose.Words.

Gäller endast vid sparning till EMF.

GDI+-sparande fungerar bara på .NET.

Standardvärdet är`sann`.

## Exempel

Visar hur man väljer en renderer när man konverterar ett dokument till .emf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// När vi sparar dokumentet som en EMF-bild kan vi skicka ett SaveOptions-objekt för att välja en renderer för bilden.
// Om vi ställer in flaggan "UseGdiEmfRenderer" till "true", kommer Aspose.Words att använda GDI+-renderaren.
// Om vi ställer in flaggan "UseGdiEmfRenderer" till "false", kommer Aspose.Words att använda sin egen metafil-renderer.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);
```

### Se även

* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
