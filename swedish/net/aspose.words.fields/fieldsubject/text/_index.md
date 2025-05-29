---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Hantera egenskapen FieldSubject Text utan ansträngning – hämta eller ställ in din ämnestext för sömlös datahantering och förbättrad användarupplevelse.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

Hämtar eller ställer in ämnestexten.

```csharp
public string Text { get; set; }
```

## Exempel

Visar hur man använder fältet ÄMNE.

```csharp
Document doc = new Document();

// Ange ett värde för dokumentets inbyggda egenskap "Ämne".
doc.BuiltInDocumentProperties.Subject = "My subject";

// Skapa ett SUBJECT-fält för att visa värdet för den inbyggda egenskapen.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// Om vi anger egenskapsvärdet Text för fältet SUBJECT och uppdaterar det, kommer fältet att
// skriv över det aktuella värdet för den inbyggda egenskapen "Ämne" med värdet för dess Text-egenskap,
// och sedan visa det nya värdet.
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### Se även

* class [FieldSubject](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
