---
title: DocumentBuilder.PushFont
linktitle: PushFont
articleTitle: PushFont
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die PushFont-Methode von DocumentBuilder die Formatierung Ihres Dokuments verbessert, indem sie Zeichenstile für einen einfachen Abruf und ein konsistentes Design speichert.
type: docs
weight: 640
url: /de/net/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder.PushFont method

Speichert die aktuelle Zeichenformatierung auf dem Stapel.

```csharp
public void PushFont()
```

## Beispiele

Zeigt, wie der Formatierungsstapel eines Dokument-Generators verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Richten Sie die Schriftformatierung ein und schreiben Sie dann den Text, der vor dem Hyperlink steht.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Behalten Sie unsere aktuelle Formatierungskonfiguration auf dem Stapel bei.
builder.PushFont();

// Ändern Sie die aktuelle Formatierung des Builders, indem Sie einen neuen Stil anwenden.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Stellen Sie die zuvor gespeicherte Schriftformatierung wieder her und entfernen Sie das Element aus dem Stapel.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Siehe auch

* property [Font](../font/)
* method [PopFont](../popfont/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
