---
title: TxtSaveOptions.AddBidiMarks
linktitle: AddBidiMarks
articleTitle: AddBidiMarks
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen AddBidiMarks i TxtSaveOptions förbättrar export av vanlig text genom att lägga till dubbelriktade markeringar för förbättrad läsbarhet och formatering.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Anger om dubbelriktade markeringar ska läggas till före varje BiDi-körning vid export i oformaterad text.

Standardvärdet är`falsk`.

```csharp
public bool AddBidiMarks { get; set; }
```

## Exempel

Visar hur man infogar Unicode-tecknet 'HÖGER-TILL-VÄNSTER-MÄRKET' (U+200F) före varje dubbelriktad körning i text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur vi sparar dokumentet som klartext.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Sätt egenskapen "AddBidiMarks" till "true" för att lägga till markeringar före körningar
// med text från höger till vänster för att indikera faktum.
// Sätt egenskapen "AddBidiMarks" till "false" för att skriva alla från vänster till höger
// och höger till vänster löper lika utan något som indikerar vilken som är vilken.
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
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
