---
title: TxtSaveOptions.ListIndentation
second_title: Aspose.Words för .NET API Referens
description: TxtSaveOptions fast egendom. Får enTxtListIndentation objekt som anger hur många och vilket tecken som ska användas för indrag av listnivåer. Som standard är det noll antal tecken 0 det betyder ingen indrag.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

Får en[`TxtListIndentation`](../../txtlistindentation/) objekt som anger hur många och vilket tecken som ska användas för indrag av listnivåer. Som standard är det noll antal tecken '\0', det betyder ingen indrag.

```csharp
public TxtListIndentation ListIndentation { get; }
```

### Exempel

Visar hur du konfigurerar listindrag när du sparar ett dokument som klartext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en lista med tre nivåer av indrag.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur vi sparar dokumentet som klartext.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Ställ in egenskapen "Character" för att tilldela ett tecken att använda
// för utfyllnad som simulerar listindrag i klartext.
txtSaveOptions.ListIndentation.Character = ' ';

// Ställ in egenskapen "Count" för att ange antalet gånger
// för att placera utfyllnadstecknet för varje listindragsnivå.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### Se även

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../txtsaveoptions/)
* hopsättning [Aspose.Words](../../../)


