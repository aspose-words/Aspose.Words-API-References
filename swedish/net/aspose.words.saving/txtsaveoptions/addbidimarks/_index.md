---
title: TxtSaveOptions.AddBidiMarks
second_title: Aspose.Words för .NET API Referens
description: TxtSaveOptions fast egendom. Anger om dubbelriktade markeringar ska läggas till före varje BiDikörning vid export i vanlig textformat.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Anger om dubbelriktade markeringar ska läggas till före varje BiDi-körning vid export i vanlig textformat.

Standardvärdet är **falsk**.

```csharp
public bool AddBidiMarks { get; set; }
```

### Exempel

Visar hur man infogar Unicode-tecken 'HÖGER-TO-VÄNSTER MARK' (U+200F) före varje dubbelriktad körning i text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur vi sparar dokumentet som klartext.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Ställ in egenskapen "AddBidiMarks" till "true" för att lägga till märken före körningar
// med text från höger till vänster för att indikera faktum.
// Ställ in egenskapen "AddBidiMarks" till "false" för att skriva allt från vänster till höger
// och höger-till-vänster löper lika mycket utan att något indikerar vilken som är vilken.
saveOptions.AddBidiMarks = addBidiMarks;

doc.Save(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt", saveOptions);

string docText = System.Text.Encoding.Unicode.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    Assert.AreEqual("\uFEFFHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    Assert.True(docText.Contains("\u200f"));
}
else
{
    Assert.AreEqual("\uFEFFHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    Assert.False(docText.Contains("\u200f"));
}
```

### Se även

* class [TxtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../txtsaveoptions/)
* hopsättning [Aspose.Words](../../../)


