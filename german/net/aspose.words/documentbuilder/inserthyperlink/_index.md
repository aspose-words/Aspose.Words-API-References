---
title: DocumentBuilder.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Dokumente mit der InsertHyperlink-Methode von DocumentBuilder und fügen Sie mühelos anklickbare Links für eine verbesserte Navigation und Benutzereinbindung hinzu.
type: docs
weight: 390
url: /de/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

Fügt einen Hyperlink in das Dokument ein.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| displayText | String | Text des Links, der im Dokument angezeigt werden soll. |
| urlOrBookmark | String | Linkziel. Kann eine URL oder der Name eines Lesezeichens im Dokument sein. Diese Methode fügt immer Apostrophe am Anfang und Ende der URL hinzu. |
| isBookmark | Boolean | `WAHR` wenn der vorherige Parameter der Name eines Lesezeichens im Dokument ist; `FALSCH` ist der vorherige Parameter eine URL. |

### Rückgabewert

A[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

## Bemerkungen

Beachten Sie, dass Sie die Schriftformatierung für den Hyperlink-Anzeigetext explizit angeben müssen, indem Sie[`Font`](../font/) Eigentum.

Diese Methode ruft intern auf[`InsertField`](../insertfield/)um ein MS Word HYPERLINK-Feld in das Dokument einzufügen.

## Beispiele

Zeigt, wie ein Hyperlink-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Fügen Sie einen Hyperlink ein und heben Sie ihn mit benutzerdefinierter Formatierung hervor.
// Der Hyperlink ist ein anklickbarer Text, der uns zum in der URL angegebenen Ort führt.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Strg + Linksklick auf den Link im Text in Microsoft Word führt uns über ein neues Webbrowserfenster zur URL.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

Zeigt, wie ein Hyperlink eingefügt wird, der auf ein lokales Lesezeichen verweist.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Fügt ein HYPERLINK-Feld ein, das auf das Lesezeichen verweist. Wir können Feldschalter übergeben
// zur Methode „InsertHyperlink“ als Teil des Arguments, das den Namen des referenzierten Lesezeichens enthält.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
