---
title: Style.BaseStyleName
second_title: Aspose.Words für .NET-API-Referenz
description: Style eigendom. Ermittelt/setzt den Namen des Stils auf dem dieser Stil basiert.
type: docs
weight: 20
url: /de/net/aspose.words/style/basestylename/
---
## Style.BaseStyleName property

Ermittelt/setzt den Namen des Stils, auf dem dieser Stil basiert.

```csharp
public string BaseStyleName { get; set; }
```

### Bemerkungen

Dies ist ein leerer String, wenn der Stil nicht auf einem anderen Stil basiert, und er kann auf einen leeren String gesetzt werden.

### Beispiele

Zeigt, wie Stilaliase verwendet werden.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Dieses Dokument enthält einen Stil namens "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Wenn der Name eines Stils mehrere Werte hat, die durch Kommas getrennt sind, ist jede Klausel ein separater Alias.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Wir können auf einen Stil mit seinem Alias und seinem Namen verweisen.
Assert.AreEqual(doc.Styles["MyStyle Alias 1"], doc.Styles["MyStyle Alias 2"]);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 2"];
builder.Write("Hello again!");

Assert.AreEqual(doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style, 
    doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style);
```

### Siehe auch

* class [Style](../)
* namensraum [Aspose.Words](../../style/)
* Montage [Aspose.Words](../../../)


