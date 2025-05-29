---
title: SvgSaveOptions.MaxImageResolution
linktitle: MaxImageResolution
articleTitle: MaxImageResolution
second_title: Aspose.Words für .NET
description: Steuern Sie die Qualität Ihrer exportierten Rasterbilder mit der Option „MaxImageResolution“ von SvgSaveOptions. Stellen Sie die Pixeldichte für optimale Ergebnisse ein. Standard: 0.
type: docs
weight: 50
url: /de/net/aspose.words.saving/svgsaveoptions/maximageresolution/
---
## SvgSaveOptions.MaxImageResolution property

Ruft einen Wert in Pixeln pro Zoll ab oder legt ihn fest, der die Auflösung exportierter Rasterbilder begrenzt. Der Standardwert ist Null.

```csharp
public int MaxImageResolution { get; set; }
```

## Bemerkungen

Wenn der Wert dieser Eigenschaft ungleich Null ist, wird die Auflösung exportierter Rasterbilder begrenzt. Das heißt, Bilder mit höherer Auflösung werden bis zum Grenzwert neu abgetastet und Bilder mit niedrigerer Auflösung werden unverändert exportiert.

Wenn der Wert dieser Eigenschaft Null ist, werden alle Rasterbilder ohne Resampling exportiert.

## Beispiele

Zeigt, wie die Grenze für die Bildauflösung festgelegt wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

### Siehe auch

* class [SvgSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
