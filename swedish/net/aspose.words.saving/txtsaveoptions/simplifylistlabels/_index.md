---
title: TxtSaveOptions.SimplifyListLabels
second_title: Aspose.Words för .NET API Referens
description: TxtSaveOptions fast egendom. Anger om programmet ska förenkla listetiketter om komplex etikettformatering inte representeras tillräckligt av vanlig text.
type: docs
weight: 70
url: /sv/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Anger om programmet ska förenkla listetiketter om komplex etikettformatering inte representeras tillräckligt av vanlig text.

Om inställt på`Sann` , numrerade listetiketter skrivs i enkelt numeriskt format och specificerade listetiketter som enkla ASCII-tecken. Standardvärdet är`falsk`.

```csharp
public bool SimplifyListLabels { get; set; }
```

### Exempel

Visar hur du ändrar utseendet på listor när du sparar ett dokument som klartext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en punktlista med fem nivåer av indrag.
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

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur vi sparar dokumentet som klartext.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Sätt egenskapen "SimplifyListLabels" till "true" för att konvertera en lista
//-symboler till enklare ASCII-tecken, som '*', 'o', '+', '>', etc.
// Sätt egenskapen "SimplifyListLabels" till "false" för att bevara så många ursprungliga listsymboler som möjligt.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

if (simplifyListLabels)
    Assert.AreEqual("* Item 1\r\n" +
                    "  > Item 2\r\n" +
                    "    + Item 3\r\n" +
                    "      - Item 4\r\n" +
                    "        o Item 5\r\n", docText);
else
    Assert.AreEqual("· Item 1\r\n" +
                    "o Item 2\r\n" +
                    "§ Item 3\r\n" +
                    "· Item 4\r\n" +
                    "o Item 5\r\n", docText);
```

### Se även

* class [TxtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../txtsaveoptions/)
* hopsättning [Aspose.Words](../../../)


