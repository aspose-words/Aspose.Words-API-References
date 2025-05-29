---
title: FieldInfo.InfoType
linktitle: InfoType
articleTitle: InfoType
second_title: Aspose.Words för .NET
description: Upptäck hur du enkelt hanterar FieldInfo InfoType-egenskaper. Ställ in eller hämta enkelt dokumenttyper för sömlös integration i dina projekt.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldinfo/infotype/
---
## FieldInfo.InfoType property

Hämtar eller anger typen av dokumentegenskapen som ska infogas.

```csharp
public string InfoType { get; set; }
```

## Exempel

Visar hur man arbetar med INFO-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange ett värde för den inbyggda egenskapen "Kommentarer" och infoga sedan ett INFO-fält för att visa egenskapens värde.
doc.BuiltInDocumentProperties.Comments = "My comment";
FieldInfo field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.Update();

Assert.AreEqual(" INFO  Comments", field.GetFieldCode());
Assert.AreEqual("My comment", field.Result);

builder.Writeln();

// Ange ett värde för fältets NewValue-egenskap och uppdatera
// fältet kommer också att skriva över motsvarande inbyggda egenskap med det nya värdet.
field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.NewValue = "New comment";
field.Update();

Assert.AreEqual(" INFO  Comments \"New comment\"", field.GetFieldCode());
Assert.AreEqual("New comment", field.Result);
Assert.AreEqual("New comment", doc.BuiltInDocumentProperties.Comments);

doc.Save(ArtifactsDir + "Field.INFO.docx");
```

### Se även

* class [FieldInfo](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
