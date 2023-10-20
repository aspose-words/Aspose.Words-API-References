---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: Aspose.Words für .NET
description: Font AutoColor eigendom. Gibt die aktuell berechnete Farbe des Texts Schwarz oder Weiß zurück die für AutoFarbe verwendet werden soll. Wenn die Farbe nicht Auto ist wird zurückgegebenColor  in C#.
type: docs
weight: 20
url: /de/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

Gibt die aktuell berechnete Farbe des Texts (Schwarz oder Weiß) zurück, die für „Auto-Farbe“ verwendet werden soll. Wenn die Farbe nicht „Auto“ ist, wird zurückgegeben[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

## Bemerkungen

Wenn Text eine „automatische Farbe“ hat, wird die tatsächliche Farbe des Texts automatisch berechnet , sodass er vor der Hintergrundfarbe lesbar ist. Wenn Sie die Hintergrundfarbe ändern, wechselt die Textfarbe in MS Word automatisch zu Schwarz oder Weiß, um die Lesbarkeit zu maximieren.

## Beispiele

Zeigt, wie Sie die Lesbarkeit verbessern können, indem Sie die Textfarbe automatisch basierend auf der Helligkeit des Hintergrunds auswählen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn das Font-Objekt eines Laufs keine Textfarbe angibt, wird dies automatisch der Fall
// Wählen Sie je nach Hintergrundfarbe entweder Schwarz oder Weiß.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// Die Standardfarbe für Text ist Schwarz. Wenn die Hintergrundfarbe dunkel ist, ist schwarzer Text schwer zu erkennen.
// Um dieses Problem zu lösen, zeigt die AutoColor-Eigenschaft diesen Text in Weiß an.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// Wenn wir den Hintergrund in eine helle Farbe ändern, wird Schwarz mehr sein
// Geeignete Textfarbe als Weiß, damit die automatische Farbe ihn in Schwarz anzeigt.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
