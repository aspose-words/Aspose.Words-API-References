---
title: ListCollection.AddSingleLevelList
linktitle: AddSingleLevelList
articleTitle: AddSingleLevelList
second_title: Aspose.Words for .NET
description: 使用 ListCollection AddSingleLevelList 方法轻松创建单级列表并将其添加到文档中，从而增强组织性和清晰度。
type: docs
weight: 60
url: /zh/net/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection.AddSingleLevelList method

根据预定义模板创建一个新的单级列表，并将其添加到文档中的列表集合中。

```csharp
public List AddSingleLevelList(ListTemplate listTemplate)
```

## 例子

展示如何根据预定义的模板创建新的单级列表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ListCollection listCollection = doc.Lists;

// 从 BulletCircle 模板创建项目符号列表。
List bulletedList = listCollection.AddSingleLevelList(ListTemplate.BulletCircle);

// 将项目符号列表写入结果文档。
builder.Writeln("Bulleted list starts below:");
builder.ListFormat.List = bulletedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// 从 NumberUppercaseLetterDot 模板创建编号列表。
List numberedList = listCollection.AddSingleLevelList(ListTemplate.NumberUppercaseLetterDot);

// 将编号列表写入结果文档。
builder.Writeln("Numbered list starts below:");
builder.ListFormat.List = numberedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Save(ArtifactsDir + "Lists.AddSingleLevelList.docx");
```

### 也可以看看

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
