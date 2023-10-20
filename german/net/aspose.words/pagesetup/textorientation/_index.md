---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words für .NET
description: PageSetup TextOrientation eigendom. Ermöglicht die AngabeTextOrientation für die gesamte Seite. Der Standardwert istHorizontal in C#.
type: docs
weight: 430
url: /de/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Ermöglicht die Angabe`TextOrientation` für die gesamte Seite. Der Standardwert istHorizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## Bemerkungen

Diese Eigenschaft wird nur für die nativen MS Word-Formate DOCX, WML, RTF und DOC unterstützt.

## Beispiele

Zeigt, wie die Textausrichtung festgelegt wird.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Setzen Sie die Eigenschaft „TextOrientation“ auf „TextOrientation.Upward“, um den gesamten Text um 90 Grad zu drehen
// nach rechts, sodass der gesamte von links nach rechts verlaufende Text jetzt von oben nach unten verläuft.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Siehe auch

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
