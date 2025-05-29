---
title: ListCollection.AddSingleLevelList
linktitle: AddSingleLevelList
articleTitle: AddSingleLevelList
second_title: Aspose.Words för .NET
description: Skapa och lägg enkelt till en lista på en nivå i ditt dokument med ListCollection AddSingleLevelList-metoden, vilket förbättrar organisationen och tydligheten.
type: docs
weight: 60
url: /sv/net/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection.AddSingleLevelList method

Skapar en ny lista på en nivå baserad på den fördefinierade mallen och lägger till den i listsamlingen i dokumentet.

```csharp
public List AddSingleLevelList(ListTemplate listTemplate)
```

## Exempel

Visar hur man skapar en ny lista på en enda nivå baserat på den fördefinierade mallen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ListCollection listCollection = doc.Lists;

// Skapar punktlistan från BulletCircle-mallen.
List bulletedList = listCollection.AddSingleLevelList(ListTemplate.BulletCircle);

// Skriver punktlistan till det resulterande dokumentet.
builder.Writeln("Bulleted list starts below:");
builder.ListFormat.List = bulletedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Skapar den numrerade listan från mallen NumberUppercaseLetterDot.
List numberedList = listCollection.AddSingleLevelList(ListTemplate.NumberUppercaseLetterDot);

// Skriver den numrerade listan till det resulterande dokumentet.
builder.Writeln("Numbered list starts below:");
builder.ListFormat.List = numberedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Save(ArtifactsDir + "Lists.AddSingleLevelList.docx");
```

### Se även

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
