---
title: Font.SizeBi
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Ruft die Schriftgröße in Punkten ab oder legt sie fest die in einem Dokument mit Schreibrichtung von rechts nach links verwendet wird.
type: docs
weight: 350
url: /de/net/aspose.words/font/sizebi/
---
## Font.SizeBi property

Ruft die Schriftgröße in Punkten ab oder legt sie fest, die in einem Dokument mit Schreibrichtung von rechts nach links verwendet wird.

```csharp
public double SizeBi { get; set; }
```

### Beispiele

Zeigt, wie separate Sätze von Schriftarteinstellungen für rechts-nach-links- und rechts-nach-links-Text definiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definieren Sie eine Reihe von Schriftarteinstellungen für von links nach rechts verlaufenden Text.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Definieren Sie einen weiteren Satz von Schriftarteinstellungen für von rechts nach links verlaufenden Text.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Wir können das Bidi-Flag verwenden, um anzuzeigen, ob der Text hinzugefügt wird
// mit dem Document Builder ist von rechts nach links. Wenn wir Text hinzufügen, wobei dieses Flag auf „true“ gesetzt ist,
// es wird mit den Schriftarteinstellungen von rechts nach links formatiert.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Setzen Sie das Flag auf false und fügen Sie dann Text von links nach rechts hinzu.
// Der Document Builder formatiert diese mit den Schriftarteinstellungen von links nach rechts.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


