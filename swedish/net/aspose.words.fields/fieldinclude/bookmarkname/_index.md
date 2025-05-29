---
title: FieldInclude.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen FieldInclude BookmarkName för att enkelt hantera bokmärken i dina dokument för förbättrad organisation och effektivitet.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldinclude/bookmarkname/
---
## FieldInclude.BookmarkName property

Hämtar eller ställer in namnet på bokmärket i dokumentet som ska inkluderas.

```csharp
public string BookmarkName { get; set; }
```

## Exempel

Visar hur man skapar ett INCLUDE-fält och anger dess egenskaper.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vi kan använda ett INCLUDE-fält för att importera en del av ett annat dokument i det lokala filsystemet.
// Bokmärket från det andra dokumentet som vi refererar till med det här fältet innehåller den importerade delen.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### Se även

* class [FieldInclude](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
