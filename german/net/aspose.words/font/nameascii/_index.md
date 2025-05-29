---
title: Font.NameAscii
linktitle: NameAscii
articleTitle: NameAscii
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Font NameAscii“, um lateinische Textschriftarten anzupassen und Ihr Design mit den Zeichencodes 0–127 für eine bessere Lesbarkeit zu verbessern.
type: docs
weight: 240
url: /de/net/aspose.words/font/nameascii/
---
## Font.NameAscii property

Gibt die Schriftart für lateinischen Text zurück oder legt sie fest (Zeichen mit Zeichencodes von 0 (Null) bis 127).

```csharp
public string NameAscii { get; set; }
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
