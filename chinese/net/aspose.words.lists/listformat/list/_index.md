---
title: ListFormat.List
linktitle: List
articleTitle: List
second_title: Aspose.Words for .NET
description: 使用 ListFormat 管理文档结构。轻松获取或设置任意段落的列表，增强文档的组织性和可读性。
type: docs
weight: 20
url: /zh/net/aspose.words.lists/listformat/list/
---
## ListFormat.List property

获取或设置此段落所属的列表。

```csharp
public List List { get; set; }
```

## 评论

分配给此属性的列表必须属于当前文档。

分配给此属性的列表不能是列表样式定义。

将此属性设置为`无效的`删除段落 中的项目符号和编号，并将列表级别编号设置为零。将此属性设置为`无效的`相当于 调用[`RemoveNumbers`](../removenumbers/)。

## 例子

展示如何将一个列表嵌套在另一个列表中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开始和结束之间添加的每个段落都将成为列表中的一个项目。
// 为标题创建大纲列表。
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// 创建一个编号列表。
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// 组成列表的每个段落都会有此标志。
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// 创建项目符号列表。
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// 恢复到编号列表。
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// 恢复到大纲列表。
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

展示如何使用列表级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开始和结束之间添加的每个段落都将成为列表中的一个项目。
// 以下是我们可以使用文档构建器创建的两种类型的列表。
// 1 - 编号列表：
// 编号列表通过对每个项目进行编号来为其段落创建逻辑顺序。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// 通过设置“ListLevelNumber”属性，我们可以增加列表级别
// 在当前列表项处开始一个独立的子列表。
// 名为“NumberDefault”的 Microsoft Word 列表模板使用数字为第一个列表级别创建列表级别。
 // 更深的列表级别使用字母和小写罗马数字。
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - 项目符号列表：
// 此列表将在每个段落前应用缩进和项目符号（“•”）。
// 此列表的更深级别将使用不同的符号，例如“■”和“○”。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 我们可以通过取消设置“列表”标志来禁用列表格式，以免将任何后续段落格式化为列表。
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### 也可以看看

* class [List](../../list/)
* class [ListFormat](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
