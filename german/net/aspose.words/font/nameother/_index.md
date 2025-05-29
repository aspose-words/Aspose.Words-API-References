---
title: Font.NameOther
linktitle: NameOther
articleTitle: NameOther
second_title: Aspose.Words für .NET
description: Entdecken Sie die Schriftart NameOther. Passen Sie Schriftarten für die Zeichencodes 128–255 einfach an und verbessern Sie so Stil und Lesbarkeit Ihres Textes. Verbessern Sie Ihr Design noch heute!
type: docs
weight: 270
url: /de/net/aspose.words/font/nameother/
---
## Font.NameOther property

Gibt die Schriftart zurück oder legt sie fest, die für Zeichen mit Zeichencodes von 128 bis 255 verwendet wird.

```csharp
public string NameOther { get; set; }
```

## Beispiele

Zeigt, wie Microsoft Word zwei verschiedene Schriftarten in einem Durchgang kombinieren kann.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nehmen wir an, wir verwenden den Builder zum Einfügen, während wir diese Schriftartkonfiguration verwenden
// enthält Zeichen innerhalb des ASCII-Zeichenbereichs. In diesem Fall
// Es werden diese Zeichen in dieser Schriftart angezeigt.
builder.Font.NameAscii = "Calibri";

// Wenn keine andere Schriftart angegeben ist, wendet der Builder diese Schriftart auch auf alle Zeichen an, die er einfügt.
Assert.AreEqual("Calibri", builder.Font.Name);

// Geben Sie eine Schriftart an, die für alle Zeichen außerhalb des ASCII-Bereichs verwendet werden soll.
// Idealerweise sollte diese Schriftart für jeden erforderlichen Nicht-ASCII-Zeichencode ein Glyph haben.
builder.Font.NameOther = "Courier New";

// Fügen Sie einen Lauf mit einem Wort ein, das aus ASCII-Zeichen besteht, und einem Wort mit allen Zeichen außerhalb dieses Bereichs.
// Jedes Zeichen wird je nach Schriftart in einer der beiden Schriftarten angezeigt.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Siehe auch

* property [Name](../name/)
* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
