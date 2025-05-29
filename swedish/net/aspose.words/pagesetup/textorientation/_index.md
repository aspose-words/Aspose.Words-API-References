---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup TextOrientation för att enkelt ställa in sidans textriktning. Anpassa din layout med alternativ utöver standardinställningen Horisontell.
type: docs
weight: 430
url: /sv/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Gör det möjligt att specificera`TextOrientation` för hela sidan. Standardvärdet ärHorizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## Anmärkningar

Den här egenskapen stöds endast för MS Words native-format DOCX, WML, RTF och DOC.

## Exempel

Visar hur man ställer in textorientering.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Ställ in egenskapen "TextOrientation" till "TextOrientation.Upward" för att rotera all text 90 grader
// till höger så att all text från vänster till höger nu går uppifrån och ner.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Se även

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
