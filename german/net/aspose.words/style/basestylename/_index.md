---
title: Style.BaseStyleName
linktitle: BaseStyleName
articleTitle: BaseStyleName
second_title: Aspose.Words für .NET
description: Style BaseStyleName eigendom. Ruft den Namen des Stils ab auf dem dieser Stil basiert bzw. legt ihn fest in C#.
type: docs
weight: 30
url: /de/net/aspose.words/style/basestylename/
---
## Style.BaseStyleName property

Ruft den Namen des Stils ab, auf dem dieser Stil basiert, bzw. legt ihn fest.

```csharp
public string BaseStyleName { get; set; }
```

## Bemerkungen

Dies ist eine leere Zeichenfolge, wenn der Stil nicht auf einem anderen Stil basiert, und er kann auf eine leere Zeichenfolge gesetzt werden.

## Beispiele

Zeigt, wie Stilaliase verwendet werden.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Dieses Dokument enthält einen Stil namens „MyStyle,MyStyle Alias 1,MyStyle Alias 2“.
// Wenn der Name eines Stils mehrere durch Kommas getrennte Werte hat, ist jede Klausel ein separater Alias.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Wir können einen Stil sowohl über seinen Alias als auch über seinen Namen referenzieren.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
