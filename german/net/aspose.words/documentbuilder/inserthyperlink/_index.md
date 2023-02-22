---
title: DocumentBuilder.InsertHyperlink
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Fügt einen Hyperlink in das Dokument ein.
type: docs
weight: 340
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
| urlOrBookmark | String | Linkziel. Kann eine URL oder der Name eines Lesezeichens innerhalb des Dokuments sein. Diese Methode fügt immer Apostrophe am Anfang und am Ende der URL hinzu. |
| isBookmark | Boolean | True, wenn der vorherige Parameter ein Name eines Lesezeichens im Dokument ist; false, wenn der vorherige Parameter eine URL ist. |

### Rückgabewert

EIN[`Field`](../../../aspose.words.fields/field/) Objekt, das das eingefügte Feld darstellt.

### Bemerkungen

Beachten Sie, dass Sie die Schriftartformatierung für den Hyperlink-Anzeigetext explizit mithilfe von angeben müssen[`Font`](../font/) Eigentum.

Diese Methode ruft intern auf[`InsertField`](../insertfield/) um ein MS Word HYPERLINK field in das Dokument einzufügen.

### Beispiele

Zeigt, wie ein Hyperlink eingefügt wird, der auf ein lokales Lesezeichen verweist.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Fügen Sie ein HYPERLINK-Feld ein, das auf das Lesezeichen verweist. Wir können Feldschalter passieren
// an die Methode "InsertHyperlink" als Teil des Arguments, das den Namen des referenzierten Lesezeichens enthält.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

Zeigt, wie ein Hyperlink-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Hyperlink einfügen und mit benutzerdefinierter Formatierung hervorheben.
// Der Hyperlink ist ein anklickbares Textstück, das uns zu der in der URL angegebenen Stelle führt.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", falsch);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Strg + Linksklick auf den Link im Text in Microsoft Word bringt uns über ein neues Webbrowser-Fenster zur URL.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


