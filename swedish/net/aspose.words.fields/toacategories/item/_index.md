---
title: ToaCategories.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Hantera dina ToaCategories-objekt enkelt. Ställ in och hämta enkelt kategorirubriker efter nummer för effektiv och smidig organisation.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/toacategories/item/
---
## ToaCategories indexer

Hämtar eller ställer in kategorirubriken efter kategorinummer.

```csharp
public string this[int number] { get; set; }
```

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

* class [ToaCategories](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
