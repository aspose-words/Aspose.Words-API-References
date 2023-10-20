---
title: ToaCategories.DefaultCategories
linktitle: DefaultCategories
articleTitle: DefaultCategories
second_title: Aspose.Words för .NET
description: ToaCategories DefaultCategories fast egendom. Hämtar standardtabellen över behörighetskategorier i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/toacategories/defaultcategories/
---
## ToaCategories.DefaultCategories property

Hämtar standardtabellen över behörighetskategorier.

```csharp
public static ToaCategories DefaultCategories { get; }
```

## Anmärkningar

Använd[`ToaCategories`](../../fieldoptions/toacategories/) egenskap för att ange tabell över auktoritetskategorier för ett enda dokument.

## Exempel

Visar hur man anger en uppsättning kategorier för TOA-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOA-fält kan filtrera sina poster efter kategorier definierade i den här samlingen.
ToaCategories toaCategories = new ToaCategories();
doc.FieldOptions.ToaCategories = toaCategories;

// Denna samling av kategorier kommer med standardvärden, som vi kan skriva över med anpassade värden.
Assert.AreEqual("Cases", toaCategories[1]);
Assert.AreEqual("Statutes", toaCategories[2]);

toaCategories[1] = "My Category 1";
toaCategories[2] = "My Category 2";

// Vi kan alltid komma åt standardvärdena via denna samling.
Assert.AreEqual("Cases", ToaCategories.DefaultCategories[1]);
Assert.AreEqual("Statutes", ToaCategories.DefaultCategories[2]);

// Infoga 2 TOA-fält. TOA-fält skapar en post för varje TA-fält i dokumentet.
// Använd "\c"-omkopplaren för att välja index för en kategori från vår samling.
// Med den här omkopplaren kommer ett TOA-fält bara att ta upp poster från TA-fält som
// har också en "\c"-växel med ett matchande kategoriindex. Varje TOA-fält kommer också att visas
// namnet på kategorin som dess "\c"-växel pekar på.
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// Infoga TOA-poster i 2 kategorier. Vårt första TOA-fält kommer att få en post,
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

* class [ToaCategories](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
