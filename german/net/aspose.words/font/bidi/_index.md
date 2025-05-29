---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font-Bidi-Eigenschaft und steuern Sie die Eigenschaften von Text von rechts nach links für eine verbesserte Lesbarkeit und Benutzerfreundlichkeit Ihrer Webdesigns.
type: docs
weight: 30
url: /de/net/aspose.words/font/bidi/
---
## Font.Bidi property

Gibt an, ob der Inhalt dieses Laufs von rechts nach links verlaufen soll.

```csharp
public bool Bidi { get; set; }
```

## Bemerkungen

Diese Eigenschaft darf, wenn aktiviert, nicht bei stark von links nach rechts verlaufendem Text verwendet werden. Jegliches Verhalten unter dieser Bedingung ist nicht spezifiziert. Diese Eigenschaft darf, wenn deaktiviert, nicht bei stark von rechts nach links verlaufendem Text verwendet werden. Jegliches Verhalten unter dieser Bedingung ist nicht spezifiziert.

Bei der Anzeige des Inhalts dieses Laufs werden alle Zeichen für die Formatierung als komplexe Skriptzeichen behandelt. Das bedeutet, dass[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) und beim Rendern dieses Laufs wird ein entsprechender Schriftartname verwendet.

Wenn der Inhalt dieses Laufs angezeigt wird, fungiert diese Eigenschaft außerdem als Rechts-nach-links-Überschreibung für Zeichen , die als „schwache Typen“ und „neutrale Typen“ klassifiziert sind.

## Beispiele

Zeigt, wie separate Sätze von Schriftarteinstellungen für Text definiert werden, der von rechts nach links und von rechts nach links verläuft.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definieren Sie einen Satz von Schrifteinstellungen für Text, der von links nach rechts verläuft.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Definieren Sie einen weiteren Satz von Schrifteinstellungen für Text, der von rechts nach links verläuft.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Wir können das Bidi-Flag verwenden, um anzugeben, ob der Text, den wir hinzufügen möchten
// mit dem Dokument-Generator erfolgt die Verarbeitung von rechts nach links. Wenn wir Text hinzufügen und dieses Flag auf true gesetzt ist,
// Es wird mit den Schrifteinstellungen von rechts nach links formatiert.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Setzen Sie das Flag auf „false“ und fügen Sie dann Text von links nach rechts hinzu.
// Der Dokumentgenerator formatiert diese mithilfe der von links nach rechts verlaufenden Schrifteinstellungen.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
