---
title: Font.BoldBi
linktitle: BoldBi
articleTitle: BoldBi
second_title: Aspose.Words für .NET
description: Font BoldBi eigendom. True wenn der Text von rechts nach links fett formatiert ist in C#.
type: docs
weight: 50
url: /de/net/aspose.words/font/boldbi/
---
## Font.BoldBi property

True, wenn der Text von rechts nach links fett formatiert ist.

```csharp
public bool BoldBi { get; set; }
```

## Beispiele

Zeigt, wie separate Sätze von Schriftarteinstellungen für Text mit der Schreibrichtung von rechts nach links und von rechts nach links definiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definieren Sie eine Reihe von Schriftarteinstellungen für Text von links nach rechts.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Definieren Sie einen weiteren Satz von Schriftarteinstellungen für Text mit der Schreibrichtung von rechts nach links.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Wir können das Bidi-Flag verwenden, um anzugeben, ob der Text hinzugefügt werden soll
// mit dem Document Builder ist von rechts nach links. Wenn wir Text hinzufügen, bei dem dieses Flag auf „true“ gesetzt ist,
// Es wird mit den Schriftarteinstellungen für die Schreibrichtung von rechts nach links formatiert.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Setzen Sie das Flag auf „false“ und fügen Sie dann von links nach rechts verlaufenden Text hinzu.
// Der Document Builder formatiert diese mit den Schriftarteinstellungen für die Schreibrichtung von links nach rechts.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
