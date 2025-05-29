---
title: SvgSaveOptions.ShowPageBorder
linktitle: ShowPageBorder
articleTitle: ShowPageBorder
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ShowPageBorder“ von SvgSaveOptions, um Ihre Seitenumrisse anzupassen. Steuern Sie Ränder mühelos – die Standardeinstellung ist „true“ für eine einfache Bedienung!
type: docs
weight: 110
url: /de/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Steuert, ob der Seitenumriss mit einem Rahmen versehen wird. Standard ist`WAHR` .

```csharp
public bool ShowPageBorder { get; set; }
```

## Beispiele

Zeigt, wie die Eigenschaften von Bildern beim Konvertieren eines DOCX-Dokuments in SVG nachgeahmt werden.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Konfigurieren Sie das SvgSaveOptions-Objekt so, dass ohne Seitenränder oder auswählbaren Text gespeichert wird.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Siehe auch

* class [SvgSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
