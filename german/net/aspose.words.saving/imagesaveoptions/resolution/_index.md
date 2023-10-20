---
title: ImageSaveOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words für .NET
description: ImageSaveOptions Resolution eigendom. Legt sowohl die horizontale als auch die vertikale Auflösung für die generierten Bilder in Punkten pro Zoll fest in C#.
type: docs
weight: 130
url: /de/net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

Legt sowohl die horizontale als auch die vertikale Auflösung für die generierten Bilder in Punkten pro Zoll fest.

```csharp
public float Resolution { set; }
```

## Bemerkungen

Diese Eigenschaft ist nur beim Speichern in Rasterbildformaten wirksam.

## Beispiele

Zeigt, wie man beim Rendern eines Dokuments in PNG eine Auflösung angibt.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Erstellen Sie ein „ImageSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
            // um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // Setzen Sie die Eigenschaft „Resolution“ auf „72“, um das Dokument mit 72 dpi darzustellen.
            options.Resolution = 72;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

            Assert.That(120000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png").Length));

#if NET48 || JAVA
            Image image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png");

            Assert.AreEqual(612, image.Width);
            Assert.AreEqual(792, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png")) 
            {
                Assert.AreEqual(612, image.Width);
                Assert.AreEqual(792, image.Height);
            }
#endif
            // Setzen Sie die Eigenschaft „Resolution“ auf „300“, um das Dokument mit 300 dpi darzustellen.
            options.Resolution = 300;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);

            Assert.That(700000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png").Length));

#if NET48 || JAVA
            image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png");

            Assert.AreEqual(2550, image.Width);
            Assert.AreEqual(3300, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png")) 
            {
                Assert.AreEqual(2550, image.Width);
                Assert.AreEqual(3300, image.Height);
            }
#endif
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
