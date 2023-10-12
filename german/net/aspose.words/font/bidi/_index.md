---
title: Font.Bidi
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Gibt an ob der Inhalt dieses Laufs RechtsnachLinksEigenschaften haben soll.
type: docs
weight: 30
url: /de/net/aspose.words/font/bidi/
---
## Font.Bidi property

Gibt an, ob der Inhalt dieses Laufs Rechts-nach-Links-Eigenschaften haben soll.

```csharp
public bool Bidi { get; set; }
```

### Bemerkungen

Wenn diese Eigenschaft aktiviert ist, darf sie nicht für stark von links nach rechts verlaufenden Text verwendet werden. Jegliches Verhalten unter dieser Bedingung ist nicht spezifiziert. Wenn diese Eigenschaft deaktiviert ist, darf sie nicht mit starkem Rechts-nach-Links-Text verwendet werden. Jegliches Verhalten unter dieser Bedingung ist nicht spezifiziert.

Wenn der Inhalt dieses Laufs angezeigt wird, werden alle Zeichen zu Formatierungszwecken als komplexe Skriptzeichen behandelt. Das bedeutet, dass[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) und ein entsprechender Schriftartname wird beim Rendern dieses Laufs verwendet.

Wenn der Inhalt dieses Laufs angezeigt wird, fungiert diese Eigenschaft außerdem als Überschreibung von rechts nach links für Zeichen , die als „schwache Typen“ und „neutrale Typen“ klassifiziert sind.

### Beispiele

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
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


