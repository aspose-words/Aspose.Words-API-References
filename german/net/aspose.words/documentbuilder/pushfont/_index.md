---
title: DocumentBuilder.PushFont
linktitle: PushFont
articleTitle: PushFont
second_title: Aspose.Words für .NET
description: DocumentBuilder PushFont methode. Speichert die aktuelle Zeichenformatierung auf dem Stapel in C#.
type: docs
weight: 600
url: /de/net/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder.PushFont method

Speichert die aktuelle Zeichenformatierung auf dem Stapel.

```csharp
public void PushFont()
```

## Beispiele

Zeigt, wie der Formatierungsstapel eines Document Builders verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Richten Sie die Schriftartformatierung ein und schreiben Sie dann den Text, der vor dem Hyperlink steht.
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

// Stellen Sie die zuvor gespeicherte Schriftartformatierung wieder her und entfernen Sie das Element vom Stapel.
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
