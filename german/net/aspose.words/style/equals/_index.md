---
title: Style.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „Style Equals“ zum Vergleichen integrierter Stile. Lernen Sie die Stile für verknüpfte und nächste Absätze kennen, um die Formatierung und Designeffizienz zu verbessern.
type: docs
weight: 220
url: /de/net/aspose.words/style/equals/
---
## Style.Equals method

Vergleicht mit dem angegebenen Stil. Stil-Istds werden nur für integrierte Stile verglichen. Stil-Standards werden nicht in den Vergleich einbezogen. Basisstil, verknüpfter Stil und nächster Absatzstil werden rekursiv verglichen.

```csharp
public bool Equals(Style style)
```

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
