---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words für .NET
description: Entdecken Sie die Textorientierungseigenschaft von PageSetup, um die Textrichtung Ihrer Seite einfach festzulegen. Passen Sie Ihr Layout mit Optionen an, die über die standardmäßige horizontale Ausrichtung hinausgehen.
type: docs
weight: 430
url: /de/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Ermöglicht die Angabe`TextOrientation` für die ganze Seite. Der Standardwert istHorizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## Bemerkungen

Diese Eigenschaft wird nur für die nativen MS Word-Formate DOCX, WML, RTF und DOC unterstützt.

## Beispiele

Zeigt, wie die Textausrichtung eingestellt wird.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Setzen Sie die Eigenschaft „TextOrientation“ auf „TextOrientation.Upward“, um den gesamten Text um 90 Grad zu drehen
// nach rechts, sodass der gesamte Text, der von links nach rechts verläuft, jetzt von oben nach unten verläuft.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Siehe auch

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
