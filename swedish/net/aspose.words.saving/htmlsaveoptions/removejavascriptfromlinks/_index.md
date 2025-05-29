---
title: HtmlSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words för .NET
description: Optimera ditt webbinnehåll med HtmlSaveOptions för att enkelt ta bort JavaScript från länkar, vilket förbättrar prestandan och förbättrar användarupplevelsen.
type: docs
weight: 410
url: /sv/net/aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/
---
## HtmlSaveOptions.RemoveJavaScriptFromLinks property

Anger om JavaScript ska tas bort från länkar. Standard är`falsk` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Anmärkningar

Om det här alternativet är aktiverat kommer alla länkar som innehåller JavaScript (t.ex. länkar med "javascript:" i href-attributet) att ersättas med "javascript:void(0)". Detta kan bidra till att förhindra potentiella säkerhetsrisker, såsom XSS-attacker.

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
