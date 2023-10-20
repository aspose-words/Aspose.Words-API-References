---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words für .NET
description: ImageSaveOptions UseGdiEmfRenderer eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob beim Speichern in EMF der MetadateiRenderer GDI oder Aspose.Words verwendet werden soll in C#.
type: docs
weight: 190
url: /de/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob beim Speichern in EMF der Metadatei-Renderer GDI+ oder Aspose.Words verwendet werden soll.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## Bemerkungen

Wenn eingestellt auf`WAHR` Es wird der GDI+-Metadatei-Renderer verwendet. Dh der Inhalt wird in das GDI+-Objekt „graphics “ geschrieben und in der Metadatei gespeichert.

Wenn eingestellt auf`FALSCH` Es wird der Metadatei-Renderer Aspose.Words verwendet. Dh Inhalte werden mit Aspose.Words direkt in das Metafile-Format geschrieben.

Wirkt sich nur beim Speichern im EMF aus.

Das GDI+-Speichern funktioniert nur unter .NET.

Der Standardwert ist`WAHR`.

## Beispiele

Zeigt, wie man beim Konvertieren eines Dokuments in .emf einen Renderer auswählt.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            // Wenn wir das Dokument als EMF-Bild speichern, können wir ein SaveOptions-Objekt übergeben, um einen Renderer für das Bild auszuwählen.
            // Wenn wir das Flag „UseGdiEmfRenderer“ auf „true“ setzen, verwendet Aspose.Words den GDI+-Renderer.
            // Wenn wir das Flag „UseGdiEmfRenderer“ auf „false“ setzen, verwendet Aspose.Words seinen eigenen Metadatei-Renderer.
            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
            saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);

            // Der GDI+-Renderer erstellt normalerweise größere Dateien.
            if (useGdiEmfRenderer)
#if NET48 || JAVA
                Assert.That(300000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#elif NET5_0_OR_GREATER
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#endif
            else
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
