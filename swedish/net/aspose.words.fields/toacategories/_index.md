---
title: ToaCategories Class
linktitle: ToaCategories
articleTitle: ToaCategories
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.ToaCategories för effektiv hantering av auktoritetsförteckningar i dina dokument. Förbättra din dokumentstrukturering!
type: docs
weight: 3190
url: /sv/net/aspose.words.fields/toacategories/
---
## ToaCategories class

Representerar en tabell över auktoritetskategorier.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class ToaCategories
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ToaCategories](toacategories/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| static [DefaultCategories](../../aspose.words.fields/toacategories/defaultcategories/) { get; } | Hämtar standardtabellen över auktoritetskategorier. |
| [Item](../../aspose.words.fields/toacategories/item/) { get; set; } | Hämtar eller ställer in kategorirubriken efter kategorinummer. |

## Exempel

Visar hur man anger en uppsättning kategorier för TOA-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOA-fält kan filtrera sina poster efter kategorier som definierats i denna samling.
ToaCategories toaCategories = new ToaCategories();
doc.FieldOptions.ToaCategories = toaCategories;

// Denna samling av kategorier har standardvärden, som vi kan skriva över med anpassade värden.
Assert.AreEqual("Cases", toaCategories[1]);
Assert.AreEqual("Statutes", toaCategories[2]);

toaCategories[1] = "My Category 1";
toaCategories[2] = "My Category 2";

// Vi kan alltid komma åt standardvärdena via den här samlingen.
Assert.AreEqual("Cases", ToaCategories.DefaultCategories[1]);
Assert.AreEqual("Statutes", ToaCategories.DefaultCategories[2]);

// Infoga 2 TOA-fält. TOA-fält skapar en post för varje TA-fält i dokumentet.
// Använd knappen "\c" för att välja index för en kategori från vår samling.
// Med den här växeln kommer ett TOA-fält endast att hämta poster från TA-fält som
// har också en "\c"-växel med ett matchande kategoriindex. Varje TOA-fält kommer också att visas
// namnet på den kategori som dess "\c"-växel pekar på.
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// Infoga TOA-poster i två kategorier. Vårt första TOA-fält kommer att få en post,
// från det andra TA-fältet vars "\c"-växel också pekar på den första kategorin.
// Det andra TOA-fältet kommer att ha två poster från de andra två TA-fälten.
builder.InsertField("TA \\c 2 \\l \"entry 1\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 1 \\l \"entry 2\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 2 \\l \"entry 3\"");

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.TOA.Categories.docx");
```

### Se även

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
