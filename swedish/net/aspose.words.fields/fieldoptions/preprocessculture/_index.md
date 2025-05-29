---
title: FieldOptions.PreProcessCulture
linktitle: PreProcessCulture
articleTitle: PreProcessCulture
second_title: Aspose.Words för .NET
description: Upptäck hur FieldOptions PreProcessCulture förbättrar din databehandling genom att anpassa fältvärdeskulturer för förbättrad noggrannhet och effektivitet.
type: docs
weight: 170
url: /sv/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Hämtar eller ställer in kulturen att förbehandla fältvärden.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

## Anmärkningar

För närvarande påverkar denna fastighet endast värdet på[`FieldDocProperty`](../../fielddocproperty/) fält.

Standardvärdet är`null` När den här egenskapen är inställd på`null` , den[`FieldDocProperty`](../../fielddocproperty/) fältets värde är preprocessed med kulturen kontrollerad av[`FieldUpdateCultureSource`](../fieldupdateculturesource/) egendom.

## Exempel

Visar hur man ställer in förprocesskulturen.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Ställ in kulturen enligt vilken vissa fält ska formatera sina visade värden.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// Fältet DOCPROPERTY visar sitt resultat formaterat enligt förprocesskulturen
// Vi har satt till tyska. Fältet visar datum/tid i formatet "dd.mm.åååå hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// Efter att ha bytt till den invarianta kulturen kommer DOCPROPERTY-fältet att använda formatet "mm/dd/åååå hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### Se även

* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
