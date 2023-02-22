---
title: DocumentBuilder.PopFont
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Ruft die zuvor auf dem Stapel gespeicherte Zeichenformatierung ab.
type: docs
weight: 560
url: /de/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

Ruft die zuvor auf dem Stapel gespeicherte Zeichenformatierung ab.

```csharp
public void PopFont()
```

### Beispiele

Zeigt, wie der Formatierungsstapel eines Dokumenterstellers verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Richten Sie die Schriftartformatierung ein und schreiben Sie dann den Text, der vor dem Hyperlink steht.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Unsere aktuelle Formatierungskonfiguration auf dem Stack beibehalten.
builder.PushFont();

// Ändern Sie die aktuelle Formatierung des Builders, indem Sie einen neuen Stil anwenden.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", falsch);

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
* method [PushFont](../pushfont/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


