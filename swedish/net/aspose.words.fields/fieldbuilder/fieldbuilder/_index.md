---
title: FieldBuilder.FieldBuilder
second_title: Aspose.Words för .NET API Referens
description: FieldBuilder byggare. Initierar en instans avFieldBuilder class.
type: docs
weight: 10
url: /sv/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

Initierar en instans av[`FieldBuilder`](../) class.

```csharp
public FieldBuilder(FieldType fieldType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldType | FieldType | Typen av fält som ska byggas. |

### Exempel

Visar hur man skapar och infogar ett fält med hjälp av en fältbyggare.

```csharp
Document doc = new Document();

// Ett bekvämt sätt att lägga till textinnehåll i ett dokument är med en dokumentbyggare.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// Fält har sin byggare, som vi kan använda för att konstruera en fältkod bit för bit.
// I det här fallet kommer vi att konstruera ett STreckkodsfält som representerar ett amerikanskt postnummer,
// och sedan infoga den framför en Run.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Se även

* enum [FieldType](../../fieldtype/)
* class [FieldBuilder](../)
* namnutrymme [Aspose.Words.Fields](../../fieldbuilder/)
* hopsättning [Aspose.Words](../../../)


