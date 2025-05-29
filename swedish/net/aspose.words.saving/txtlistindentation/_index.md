---
title: TxtListIndentation Class
linktitle: TxtListIndentation
articleTitle: TxtListIndentation
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.TxtListIndentation för att anpassa listindragningsnivåer för sömlös export av textformat. Förbättra formateringen av din dokument!
type: docs
weight: 6450
url: /sv/net/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class

Anger hur listnivåer är indragna när dokumentet exporteras tillText format.

För att lära dig mer, besök[Spara ett dokument](https://docs.aspose.com/words/net/save-a-document/) dokumentationsartikel.

```csharp
public class TxtListIndentation
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [TxtListIndentation](txtlistindentation/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Character](../../aspose.words.saving/txtlistindentation/character/) { get; set; } | Hämtar eller anger vilket tecken som ska användas för att indentera listnivåer. Standardvärdet är '\0', det betyder att det inte finns någon indentering. |
| [Count](../../aspose.words.saving/txtlistindentation/count/) { get; set; } | Hämtar eller anger hur många[`Character`](./character/)att använda som indentering per listnivå. Standardvärdet är 0, det betyder ingen indentering. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
