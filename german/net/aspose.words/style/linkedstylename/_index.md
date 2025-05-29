---
title: Style.LinkedStyleName
linktitle: LinkedStyleName
articleTitle: LinkedStyleName
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die Eigenschaft „LinkedStyleName“ formatieren, verknüpfte Stile einfach verwalten und Ihren Design-Workflow durch nahtlose Integration verbessern.
type: docs
weight: 90
url: /de/net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

Ruft den Namen des[`Style`](../) mit diesem verknüpft. Gibt einen leeren String zurück, wenn keine Stile verknüpft sind.

```csharp
public string LinkedStyleName { get; set; }
```

## Bemerkungen

Es ist lediglich zulässig, den Absatzstil mit dem Zeichenstil zu verknüpfen und umgekehrt.

Das Festlegen von LinkedStyleName für den aktuellen Stil führt automatisch zum Festlegen von LinkedStyleName für den verknüpften Stil.

Das Zuweisen der leeren Zeichenfolge entspricht dem Aufheben der Verknüpfung des zuvor verknüpften Stils.

## Beispiele

Zeigt, wie Stile untereinander verknüpft werden.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];

Style styleHeading1Char = doc.Styles.Add(StyleType.Character, "Heading 1 Char");
styleHeading1Char.Font.Name = "Verdana";
styleHeading1Char.Font.Bold = true;
styleHeading1Char.Font.Border.LineStyle = LineStyle.Dot;
styleHeading1Char.Font.Border.LineWidth = 15;

styleHeading1.LinkedStyleName = "Heading 1 Char";

Assert.AreEqual("Heading 1 Char", styleHeading1.LinkedStyleName);
Assert.AreEqual("Heading 1", styleHeading1Char.LinkedStyleName);
```

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
