---
title: Font.NameAscii
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Gibt die für lateinischen Text verwendete Schriftart zurück oder legt sie fest Zeichen mit Zeichencodes von 0 Null bis 127.
type: docs
weight: 240
url: /de/net/aspose.words/font/nameascii/
---
## Font.NameAscii property

Gibt die für lateinischen Text verwendete Schriftart zurück oder legt sie fest (Zeichen mit Zeichencodes von 0 (Null) bis 127).

```csharp
public string NameAscii { get; set; }
```

### Beispiele

Zeigt, wie Microsoft Word zwei verschiedene Schriftarten in einem Durchgang kombinieren kann.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Angenommen, ein Lauf, den wir mit dem Builder einfügen, während wir diese Schriftartenkonfiguration verwenden
// enthält Zeichen innerhalb des ASCII-Zeichenbereichs. In diesem Fall,
// Es werden diese Zeichen mit dieser Schriftart angezeigt.
builder.Font.NameAscii = "Calibri";

// Wenn keine andere Schriftart angegeben ist, wendet der Builder diese Schriftart auch auf alle Zeichen an, die er einfügt.
Assert.AreEqual("Calibri", builder.Font.Name);

// Geben Sie eine Schriftart an, die für alle Zeichen außerhalb des ASCII-Bereichs verwendet werden soll.
// Idealerweise sollte diese Schriftart für jeden erforderlichen Nicht-ASCII-Zeichencode ein Glyph haben.
builder.Font.NameOther = "Courier New";

// Einen Lauf mit einem Wort bestehend aus ASCII-Zeichen und einem Wort mit allen Zeichen außerhalb dieses Bereichs einfügen.
// Jedes Zeichen wird abhängig von einer der Schriftarten angezeigt.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Siehe auch

* property [Name](../name/)
* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


