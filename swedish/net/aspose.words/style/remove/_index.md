---
title: Style.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words för .NET
description: Ta enkelt bort oönskade stilar från ditt dokument med metoden Style Remove. Förbättra ditt innehålls utseende och bibehåll konsekvens!
type: docs
weight: 230
url: /sv/net/aspose.words/style/remove/
---
## Style.Remove method

Tar bort den angivna stilen från dokumentet.

```csharp
public void Remove()
```

## Anmärkningar

Borttagning av stil har följande effekter på dokumentmodellen:

* Alla referenser till stilen tas bort från motsvarande stycken, avsnitt och tabeller.
* Om basstilen tas bort flyttas dess formatering till understilar.
* Om stilen som ska tas bort har en länkad stil, tas båda dessa bort.

## Exempel

Visar hur man skapar och tillämpar en anpassad stil.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Omdefiniera stil automatiskt.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en av formaten från dokumentet på stycket som dokumentbyggaren skapar.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Ta bort vår anpassade stil från dokumentets stilsamling.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// All text som använde en borttagen stil återgår till standardformateringen.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Se även

* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
