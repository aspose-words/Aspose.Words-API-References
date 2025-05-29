---
title: TxtSaveOptions.ListIndentation
linktitle: ListIndentation
articleTitle: ListIndentation
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ListIndentation i TxtSaveOptions, som anpassar listindrag för förbättrad läsbarhet. Kontrollera tecken och nivåer utan ansträngning!
type: docs
weight: 30
url: /sv/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

Får en[`TxtListIndentation`](../../txtlistindentation/)objekt som anger hur många och vilka tecken som ska användas för indentering av listnivåer. Som standard är det noll antal tecken '\0', det betyder ingen indentering.

```csharp
public TxtListIndentation ListIndentation { get; }
```

## Exempel

Visar hur man konfigurerar listindrag när man sparar ett dokument som klartext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en lista med tre nivåer av indentering.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur vi sparar dokumentet som klartext.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Ange egenskapen "Tecken" för att tilldela ett tecken att använda
// för utfyllnad som simulerar listindrag i klartext.
txtSaveOptions.ListIndentation.Character = ' ';

// Ange antalet gånger med egenskapen "Count"
// för att placera utfyllnadstecknet för varje listindragsnivå.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");
string newLine= Environment.NewLine;

Assert.AreEqual($"1. Item 1{newLine}" +
                $"   a. Item 2{newLine}" +
                $"      i. Item 3{newLine}", docText);
```

### Se även

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
