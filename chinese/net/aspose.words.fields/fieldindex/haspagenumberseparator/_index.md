---
title: FieldIndex.HasPageNumberSeparator
second_title: Aspose.Words for .NET API 参考
description: FieldIndex 财产. 获取一个值该值指示是否通过字段的代码覆盖页码分隔符
type: docs
weight: 50
url: /zh/net/aspose.words.fields/fieldindex/haspagenumberseparator/
---
## FieldIndex.HasPageNumberSeparator property

获取一个值，该值指示是否通过字段的代码覆盖页码分隔符。

```csharp
public bool HasPageNumberSeparator { get; }
```

### 例子

显示如何在 INDEX 字段中编辑页码分隔符。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目都会在左侧显示 XE 字段的 Text 属性值，
// 以及右侧包含 XE 字段的页码。
// INDEX 条目将在“文本”属性中对具有匹配值的 XE 字段进行分组
// 进入一个条目，而不是为每个 XE 字段创建一个条目。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// 如果我们的 INDEX 字段有一组 XE 字段的条目，
// 此条目将显示包含属于该组的 XE 字段的每个页面的数量。
// 我们可以设置自定义分隔符来自定义这些页码的外观。
index.PageNumberSeparator = ", on page(s) ";
index.PageNumberListSeparator = " & ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.GetFieldCode());
Assert.True(index.HasPageNumberSeparator);

// 插入这些 XE 字段后，INDEX 字段将显示“第一个条目，在第 2 & 3 & 4 页上”。
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

Assert.AreEqual(" XE  \"First entry\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageNumberList.docx");
```

### 也可以看看

* class [FieldIndex](../)
* 命名空间 [Aspose.Words.Fields](../../fieldindex/)
* 部件 [Aspose.Words](../../../)


