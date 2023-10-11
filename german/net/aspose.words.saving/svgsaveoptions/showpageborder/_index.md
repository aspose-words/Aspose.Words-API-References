---
title: SvgSaveOptions.ShowPageBorder
second_title: Aspose.Words für .NET-API-Referenz
description: SvgSaveOptions eigendom. Steuert ob dem Umriss der Seite ein Rahmen hinzugefügt wird. Standard istWAHR .
type: docs
weight: 80
url: /de/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Steuert, ob dem Umriss der Seite ein Rahmen hinzugefügt wird. Standard ist`WAHR` .

```csharp
public bool ShowPageBorder { get; set; }
```

### Beispiele

Zeigt, wie die Eigenschaften von Bildern beim Konvertieren eines .docx-Dokuments in .svg nachgeahmt werden.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Konfigurieren Sie das SVGSaveOptions-Objekt zum Speichern ohne Seitenränder oder auswählbaren Text.
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
* namensraum [Aspose.Words.Saving](../../svgsaveoptions/)
* Montage [Aspose.Words](../../../)


