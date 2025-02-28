---
title: ListCollection.AddSingleLevelList
linktitle: AddSingleLevelList
articleTitle: AddSingleLevelList
second_title: Aspose.Words for .NET
description: Effortlessly create and add a single-level list to your document with the ListCollection AddSingleLevelList method, enhancing organization and clarity.
type: docs
weight: 60
url: /net/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection.AddSingleLevelList method

Creates a new single level list based on the predefined template and adds it to the list collection in the document.

```csharp
public List AddSingleLevelList(ListTemplate listTemplate)
```

## Examples

Shows how to create a new single level list based on the predefined template.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ListCollection listCollection = doc.Lists;

// Creates the bulleted list from BulletCircle template.
List bulletedList = listCollection.AddSingleLevelList(ListTemplate.BulletCircle);

// Writes the bulleted list to the resulting document.
builder.Writeln("Bulleted list starts below:");
builder.ListFormat.List = bulletedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Creates the numbered list from NumberUppercaseLetterDot template.
List numberedList = listCollection.AddSingleLevelList(ListTemplate.NumberUppercaseLetterDot);

// Writes the numbered list to the resulting document.
builder.Writeln("Numbered list starts below:");
builder.ListFormat.List = numberedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Save(ArtifactsDir + "Lists.AddSingleLevelList.docx");
```

### See Also

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)
