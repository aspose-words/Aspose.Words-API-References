---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: Aspose.Words för .NET
description: TxtSaveOptions PreserveTableLayout fast egendom. Anger om programmet ska försöka bevara layout av tabeller när det sparas i vanlig textformat. Standardvärdet ärfalsk  i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Anger om programmet ska försöka bevara layout av tabeller när det sparas i vanlig textformat. Standardvärdet är`falsk` .

```csharp
public bool PreserveTableLayout { get; set; }
```

## Exempel

Visar hur man bevarar layouten för tabeller vid konvertering till klartext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1");
builder.InsertCell();
builder.Write("Row 2, cell 2");
builder.EndTable();

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur vi sparar dokumentet som klartext.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Ställ in egenskapen "PreserveTableLayout" till "true" för att använda blankstegsutfyllnad på innehållet
// av det utgående klartextdokumentet för att bevara så mycket av tabellens layout som möjligt.
// Ställ in egenskapen "PreserveTableLayout" till "false" för att spara alla tabellers innehåll
// som en kontinuerlig textdel, med bara en ny rad för varje rad.
txtSaveOptions.PreserveTableLayout = preserveTableLayout;

doc.Save(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
    Assert.AreEqual("Row 1, cell 1                                            Row 1, cell 2\r\n" +
                    "Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
else
    Assert.AreEqual("Row 1, cell 1\r" +
                    "Row 1, cell 2\r" +
                    "Row 2, cell 1\r" +
                    "Row 2, cell 2\r\r\n", docText);
```

### Se även

* class [TxtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
