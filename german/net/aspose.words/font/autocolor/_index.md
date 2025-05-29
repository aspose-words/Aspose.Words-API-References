---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font AutoColor-Eigenschaft und wählen Sie die aktuelle Textfarbe (Schwarz oder Weiß) für automatische Farbanpassungen. Optimieren Sie Ihr Design mühelos!
type: docs
weight: 20
url: /de/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

Gibt die aktuell berechnete Farbe des Textes (schwarz oder weiß) zurück, die für „Auto-Farbe“ verwendet werden soll. Wenn die Farbe nicht „auto“ ist, wird Folgendes zurückgegeben[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

## Bemerkungen

Bei automatischer Farbgebung wird die tatsächliche Textfarbe automatisch berechnet, sodass der Text vor der Hintergrundfarbe lesbar ist. Wenn Sie die Hintergrundfarbe ändern, wird die Textfarbe in MS Word automatisch auf Schwarz oder Weiß umgestellt, um die Lesbarkeit zu optimieren.

## Beispiele

Zeigt, wie die Lesbarkeit durch die automatische Auswahl der Textfarbe basierend auf der Helligkeit des Hintergrunds verbessert werden kann.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn das Font-Objekt eines Laufs keine Textfarbe angibt, wird es automatisch
// Wählen Sie je nach Hintergrundfarbe entweder Schwarz oder Weiß aus.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// Die Standardfarbe für Text ist Schwarz. Bei einer dunklen Hintergrundfarbe ist schwarzer Text schwer zu erkennen.
// Um dieses Problem zu lösen, zeigt die AutoColor-Eigenschaft diesen Text in Weiß an.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// Wenn wir den Hintergrund in eine helle Farbe ändern, ist Schwarz eine
// geeignete Textfarbe als Weiß, damit die automatische Farbe ihn in Schwarz anzeigt.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
