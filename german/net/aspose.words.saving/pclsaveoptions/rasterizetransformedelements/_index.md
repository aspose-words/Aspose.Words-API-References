---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words für .NET
description: PclSaveOptions RasterizeTransformedElements eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob komplexe transformierte Elemente vor dem Speichern im PCLDokument gerastert werden sollen. Die Standardeinstellung istWAHR  in C#.
type: docs
weight: 30
url: /de/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob komplexe transformierte Elemente vor dem Speichern im PCL-Dokument gerastert werden sollen. Die Standardeinstellung ist`WAHR` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Bemerkungen

PCL unterstützt einige Transformationen, die von Aspose Words verwendet werden, nicht. Z. B. gedrehte, geneigte Bilder und Texturpinsel. Um solche Elemente richtig zu rendern, wird der Rasterisierungsprozess verwendet, d. h. Speichern im Bild und Ausschneiden. Dieser Prozess kann zusätzliche Zeit und Speicher beanspruchen. Wenn das Flag auf gesetzt ist`FALSCH` , einige Inhalte in der Ausgabe können im Vergleich zum Quelldokument unterschiedlich sein

## Beispiele

Zeigt, wie man komplexe Elemente rastern kann, während man ein Dokument in PCL speichert.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### Siehe auch

* class [PclSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
