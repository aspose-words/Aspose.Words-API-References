---
title: Font.BoldBi
linktitle: BoldBi
articleTitle: BoldBi
second_title: Aspose.Words für .NET
description: Entdecken Sie die BoldBi-Eigenschaft, die sicherstellt, dass von rechts nach links geschriebener Text fett angezeigt wird, wodurch die Lesbarkeit und das Benutzererlebnis für verschiedene Sprachen verbessert werden.
type: docs
weight: 50
url: /de/net/aspose.words/font/boldbi/
---
## Font.BoldBi property

Wahr, wenn der von rechts nach links verlaufende Text fett formatiert ist.

```csharp
public bool BoldBi { get; set; }
```

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
