---
title: FieldInclude.TextConverter
linktitle: TextConverter
articleTitle: TextConverter
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldInclude TextConverter – hantera enkelt filformatkonverteringar med anpassningsbara textkonverterarnamn för förbättrad arbetsflödeseffektivitet.
type: docs
weight: 50
url: /sv/net/aspose.words.fields/fieldinclude/textconverter/
---
## FieldInclude.TextConverter property

Hämtar eller anger namnet på textkonverteraren för formatet för den inkluderade filen.

```csharp
public string TextConverter { get; set; }
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
