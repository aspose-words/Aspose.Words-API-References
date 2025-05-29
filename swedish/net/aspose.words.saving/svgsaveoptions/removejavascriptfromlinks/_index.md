---
title: SvgSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words för .NET
description: Optimera SVG-filer med SvgSaveOptions, ta enkelt bort JavaScript från länkar för renare kod. Förbättra prestanda och säkerhet med denna enkla inställning!
type: docs
weight: 60
url: /sv/net/aspose.words.saving/svgsaveoptions/removejavascriptfromlinks/
---
## SvgSaveOptions.RemoveJavaScriptFromLinks property

Anger om JavaScript ska tas bort från länkar. Standard är`falsk` . Om det här alternativet är aktiverat kommer alla länkar som innehåller JavaScript att ersättas med "javascript:void(0)".

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Exempel

Visar hur man tar bort JavaScript från länkarna (svg).

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

### Se även

* class [SvgSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
