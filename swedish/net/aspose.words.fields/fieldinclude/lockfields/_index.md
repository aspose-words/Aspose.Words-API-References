---
title: FieldInclude.LockFields
linktitle: LockFields
articleTitle: LockFields
second_title: Aspose.Words för .NET
description: FieldInclude LockFields fast egendom. Hämtar eller ställer in om fält i det inkluderade dokumentet ska förhindras från att uppdateras i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldinclude/lockfields/
---
## FieldInclude.LockFields property

Hämtar eller ställer in om fält i det inkluderade dokumentet ska förhindras från att uppdateras.

```csharp
public bool LockFields { get; set; }
```

## Exempel

Visar hur man skapar ett INKLUDERA-fält och ställer in dess egenskaper.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vi kan använda ett INCLUDE-fält för att importera en del av ett annat dokument i det lokala filsystemet.
// Bokmärket från det andra dokumentet som vi refererar till med det här fältet innehåller denna importerade del.
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
