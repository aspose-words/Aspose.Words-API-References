---
title: Style.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words för .NET
description: Style Equals metod. Jämförs med den angivna stilen. Stilar Istds jämförs endast för inbyggda stilar. Standardinställningar för format ingår inte i jämförelsen. Basstil länkad stil och nästa styckestil jämförs rekursivt i C#.
type: docs
weight: 180
url: /sv/net/aspose.words/style/equals/
---
## Style.Equals method

Jämförs med den angivna stilen. Stilar Istds jämförs endast för inbyggda stilar. Standardinställningar för format ingår inte i jämförelsen. Basstil, länkad stil och nästa styckestil jämförs rekursivt.

```csharp
public bool Equals(Style style)
```

## Exempel

Visar hur man använder stilalias.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Det här dokumentet innehåller en stil som heter "MyStyle, MyStyle Alias 1, MyStyle Alias 2".
// Om en stils namn har flera värden separerade med kommatecken, är varje sats ett separat alias.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Vi kan referera till en stil med dess alias, såväl som dess namn.
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

### Se även

* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
