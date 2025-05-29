---
title: ViewOptions.DisplayBackgroundShape
linktitle: DisplayBackgroundShape
articleTitle: DisplayBackgroundShape
second_title: Aspose.Words för .NET
description: Upptäck egenskapen DisplayBackgroundShape i ViewOptions för att förbättra din utskriftslayout med anpassningsbara bakgrundsformer för ett elegant utseende.
type: docs
weight: 10
url: /sv/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

Styr visningen av bakgrundsformen i utskriftslayoutvyn.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

## Exempel

Visar hur man döljer/visar dokumentbakgrundsbilder i vyalternativen.

```csharp
// Använd en HTML-sträng för att skapa ett nytt dokument med en platt bakgrundsfärg.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// Källkoden för dokumentet har en bakgrund med en platt färg,
// vars närvaro sätter flaggan "DisplayBackgroundShape" till "sant".
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// Behåll "DisplayBackgroundShape" som "true" för att få dokumentet att visa bakgrundsfärgen.
// Detta kan påverka vissa textfärger för att förbättra synligheten.
// Sätt "DisplayBackgroundShape" till "false" för att inte visa bakgrundsfärgen.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### Se även

* class [ViewOptions](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
