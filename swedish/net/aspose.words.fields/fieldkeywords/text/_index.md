---
title: FieldKeywords.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Hantera dina FieldKeywords enkelt! Få åtkomst till och anpassa nyckelordstexten för optimal SEO-prestanda och förbättrad synlighet.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Hämtar eller ställer in texten för nyckelorden.

```csharp
public string Text { get; set; }
```

## Exempel

Visar för att infoga ett NYCKELORD-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till några nyckelord, även kallade "taggar" i Utforskaren.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// Fältet NYCKELORD visar värdet för den här egenskapen.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// Anger ett värde för fältets Text-egenskap,
// och att sedan uppdatera fältet kommer även att skriva över motsvarande inbyggda egenskap med det nya värdet.
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### Se även

* class [FieldKeywords](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
