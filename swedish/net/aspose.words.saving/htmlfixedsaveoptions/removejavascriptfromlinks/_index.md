---
title: HtmlFixedSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words för .NET
description: Optimera din HTML med funktionen HtmlFixedSaveOptions RemoveJavaScriptFromLinks. Förbättra säkerheten genom att enkelt ta bort JavaScript från länkar.
type: docs
weight: 140
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/
---
## HtmlFixedSaveOptions.RemoveJavaScriptFromLinks property

Anger om JavaScript ska tas bort från länkar. Standard är`falsk` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Anmärkningar

Om det här alternativet är aktiverat kommer alla länkar som innehåller JavaScript (t.ex. länkar med "javascript:" i href-attributet) att ersättas med "javascript:void(0)". Detta kan bidra till att förhindra potentiella säkerhetsrisker, såsom XSS-attacker.

## Exempel

Visar hur man tar bort JavaScript från länkarna.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

Visar hur man tar bort JavaScript från länkar för HTML-fixerade dokument.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
