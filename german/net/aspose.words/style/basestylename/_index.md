---
title: Style.BaseStyleName
linktitle: BaseStyleName
articleTitle: BaseStyleName
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die BaseStyleName-Eigenschaft anpassen, um Ihr Design zu verbessern. Rufen Sie den Stilnamen einfach ab oder legen Sie ihn fest, um die Optik zu verbessern!
type: docs
weight: 30
url: /de/net/aspose.words/style/basestylename/
---
## Style.BaseStyleName property

Ruft den Namen des Stils ab/legt ihn fest, auf dem dieser Stil basiert.

```csharp
public string BaseStyleName { get; set; }
```

## Bemerkungen

Dies ist eine leere Zeichenfolge, wenn der Stil nicht auf einem anderen Stil basiert und auf eine leere Zeichenfolge gesetzt werden kann.

## Beispiele

Zeigt, wie Stilaliase verwendet werden.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Dieses Dokument enthält einen Stil mit dem Namen „MyStyle,MyStyle Alias 1,MyStyle Alias 2“.
// Wenn der Name eines Stils mehrere durch Kommas getrennte Werte hat, ist jede Klausel ein separater Alias.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Wir können auf einen Stil sowohl über seinen Alias als auch über seinen Namen verweisen.
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
