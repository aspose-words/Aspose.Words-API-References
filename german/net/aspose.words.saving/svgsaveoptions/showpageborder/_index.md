---
title: SvgSaveOptions.ShowPageBorder
second_title: Aspose.Words für .NET-API-Referenz
description: SvgSaveOptions eigendom. Steuert ob der Kontur der Seite ein Rahmen hinzugefügt wird. Standard istStimmt .
type: docs
weight: 80
url: /de/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Steuert, ob der Kontur der Seite ein Rahmen hinzugefügt wird. Standard ist`Stimmt` .

```csharp
public bool ShowPageBorder { get; set; }
```

### Beispiele

Zeigt, wie die Eigenschaften von Bildern beim Konvertieren eines .docx-Dokuments in .svg nachgeahmt werden.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Konfigurieren Sie das SvgSaveOptions-Objekt so, dass es ohne Seitenränder oder auswählbaren Text gespeichert wird.
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


