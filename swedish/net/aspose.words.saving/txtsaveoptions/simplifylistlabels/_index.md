---
title: TxtSaveOptions.SimplifyListLabels
linktitle: SimplifyListLabels
articleTitle: SimplifyListLabels
second_title: Aspose.Words för .NET
description: Upptäck hur TxtSaveOptions funktion SimplifyListLabels förbättrar tydligheten genom att effektivisera komplexa listetiketter för förbättrad textrepresentation.
type: docs
weight: 70
url: /sv/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Anger om programmet ska förenkla listetiketter om komplex etikettformatering inte representeras tillräckligt med vanlig text.

Om inställd på`sann` , numrerade listetiketter skrivs i enkelt numeriskt format och specificerade listetiketter som enkla ASCII-tecken. Standardvärdet är`falsk`.

```csharp
public bool SimplifyListLabels { get; set; }
```

## Exempel

Visar hur man ändrar utseendet på listor när man sparar ett dokument som klartext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en punktlista med fem nivåer av indentering.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent();
builder.Writeln("Item 3");
builder.ListFormat.ListIndent();
builder.Writeln("Item 4");
builder.ListFormat.ListIndent();
builder.Write("Item 5");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur vi sparar dokumentet som klartext.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Sätt egenskapen "SimplifyListLabels" till "true" för att konvertera vissa listor
// symboler till enklare ASCII-tecken, såsom '*', 'o', '+', '>', etc.
// Sätt egenskapen "SimplifyListLabels" till "false" för att bevara så många ursprungliga listsymboler som möjligt.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

string newLine = Environment.NewLine;

if (simplifyListLabels)
    Assert.AreEqual($"* Item 1{newLine}" +
                    $"  > Item 2{newLine}" +
                    $"    + Item 3{newLine}" +
                    $"      - Item 4{newLine}" +
                    $"        o Item 5{newLine}", docText);
else
    Assert.AreEqual($"· Item 1{newLine}" +
                    $"o Item 2{newLine}" +
                    $"§ Item 3{newLine}" +
                    $"· Item 4{newLine}" +
                    $"o Item 5{newLine}", docText);
```

### Se även

* class [TxtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
