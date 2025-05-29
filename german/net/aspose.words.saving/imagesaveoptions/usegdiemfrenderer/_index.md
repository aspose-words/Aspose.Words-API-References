---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words für .NET
description: Optimieren Sie die EMF-Speicherung mit ImageSaveOptions. Steuern Sie die GDI- oder Aspose.Words-Renderer-Einstellungen für verbesserte Bildqualität und Leistung.
type: docs
weight: 190
url: /de/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob beim Speichern in EMF der GDI+- oder Aspose.Words-Metadatei-Renderer verwendet werden soll.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## Bemerkungen

Wenn eingestellt auf`WAHR` Es wird ein GDI+-Metadatei-Renderer verwendet. D. h., der Inhalt wird in das GDI+-Graphics -Objekt geschrieben und in der Metadatei gespeichert.

Wenn eingestellt auf`FALSCH` Der Aspose.Words-Metadatei-Renderer wird verwendet. D. h., Inhalte werden mit Aspose.Words direkt in das Metadateiformat geschrieben.

Hat nur beim Speichern im EMF eine Wirkung.

Das Speichern mit GDI+ funktioniert nur unter .NET.

Der Standardwert ist`WAHR`.

## Beispiele

Zeigt, wie Sie beim Konvertieren eines Dokuments in das EMF-Format einen Renderer auswählen.

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
```

### Siehe auch

* class [ImageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
