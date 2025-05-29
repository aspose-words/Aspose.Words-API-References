---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words für .NET
description: Steuern Sie die Rasterung komplexer Elemente in PCL-Dokumenten mit PclSaveOptions. Verwalten Sie Bildqualität und Dateigröße ganz einfach für optimale Ergebnisse.
type: docs
weight: 30
url: /de/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob komplexe transformierte Elemente vor dem Speichern in einem PCL-Dokument gerastert werden sollen. Der Standardwert ist`WAHR` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Bemerkungen

PCL unterstützt einige Transformationen, die von Aspose Words verwendet werden, nicht. Z. B. gedrehte, verzerrte Bilder und Texturpinsel. Um solche Elemente korrekt darzustellen, wird ein Rasterungsprozess verwendet, d. h. Speichern im Bild und Ausschneiden. Dieser Prozess kann zusätzliche Zeit und Speicherplatz beanspruchen. Wenn das Flag auf gesetzt ist`FALSCH` , einige Inhalte in der Ausgabe können sich vom Quelldokument unterscheiden.

## Beispiele

Zeigt, wie komplexe Elemente beim Speichern eines Dokuments im PCL-Format gerastert werden.

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
