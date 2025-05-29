---
title: FieldDocVariable.VariableName
linktitle: VariableName
articleTitle: VariableName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldDocVariable VariableName för att enkelt hantera dokumentvariabler. Förenkla hämtning och förbättra din dokumenthantering idag!
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fielddocvariable/variablename/
---
## FieldDocVariable.VariableName property

Hämtar eller anger namnet på dokumentvariabeln som ska hämtas.

```csharp
public string VariableName { get; set; }
```

## Exempel

Visar hur man använder DOCPROPERTY-fält för att visa dokumentegenskaper och variabler.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer två sätt att använda DOCPROPERTY-fält.
// 1 - Visa en inbyggd egenskap:
// Ange ett anpassat värde för den inbyggda egenskapen "Kategori" och infoga sedan ett DOCPROPERTY-fält som refererar till det.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.AreEqual(" DOCPROPERTY Category ", fieldDocProperty.GetFieldCode());
Assert.AreEqual("My category", fieldDocProperty.Result);

builder.InsertParagraph();

// 2 - Visa en anpassad dokumentvariabel:
// Definiera en anpassad variabel och referera sedan till den variabeln med ett DOCPROPERTY-fält.
Assert.AreEqual(0, doc.Variables.Count);
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.AreEqual(" DOCVARIABLE  \"My Variable\"", fieldDocVariable.GetFieldCode());
Assert.AreEqual("My variable's value", fieldDocVariable.Result);

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### Se även

* class [FieldDocVariable](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
