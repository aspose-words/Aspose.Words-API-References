---
title: Style.Equals
second_title: Aspose.Words für .NET-API-Referenz
description: Style methode. Vergleicht mit dem angegebenen Stil. IstdsStile werden nur für integrierte Stile verglichen. Standardwerte für Stile werden nicht im Vergleich berücksichtigt. Basisstil verknüpfter Stil und Stil für den nächsten Absatz werden rekursiv verglichen.
type: docs
weight: 190
url: /de/net/aspose.words/style/equals/
---
## Style.Equals method

Vergleicht mit dem angegebenen Stil. Istds-Stile werden nur für integrierte Stile verglichen. Standardwerte für Stile werden nicht im Vergleich berücksichtigt. Basisstil, verknüpfter Stil und Stil für den nächsten Absatz werden rekursiv verglichen.

```csharp
public bool Equals(Style style)
```

### Beispiele

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
* namensraum [Aspose.Words](../../style/)
* Montage [Aspose.Words](../../../)


