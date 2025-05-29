---
title: FieldSet.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldSet BookmarkName för att enkelt hantera och anpassa dina bokmärken. Förbättra din applikations navigering med denna viktiga funktion!
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldset/bookmarkname/
---
## FieldSet.BookmarkName property

Hämtar eller anger namnet på bokmärket.

```csharp
public string BookmarkName { get; set; }
```

## Exempel

Visar hur man skapar bokmärkt text med ett SET-fält och sedan visar den i dokumentet med ett REF-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Namnge bokmärkt text med ett SET-fält.
// Detta fält refererar till "bokmärket", inte en bokmärkesstruktur som visas i texten, utan en namngiven variabel.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Referera till bokmärket med namn i ett REF-fält och visa dess innehåll.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### Se även

* class [FieldSet](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
