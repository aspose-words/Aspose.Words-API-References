---
title: FieldTC.TypeIdentifier
second_title: Aspose.Words for .NET API 参考
description: FieldTC 财产. 获取或设置该字段的类型标识符通常是字母
type: docs
weight: 50
url: /zh/net/aspose.words.fields/fieldtc/typeidentifier/
---
## FieldTC.TypeIdentifier property

获取或设置该字段的类型标识符（通常是字母）。

```csharp
public string TypeIdentifier { get; set; }
```

### 例子

展示如何插入一个 TOC 字段，并过滤哪些 TC 字段最终成为条目。

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入一个 TOC 字段，这会将所有 TC 字段编译成一个目录。
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // 配置该字段只获取“A”类型的TC条目，以及1到3之间的条目级别。
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // 这两个条目将出现在表格中。
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // 此条目将从表中省略，因为它的类型与“A”不同。
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // 此条目将从表中省略，因为它具有 1-3 范围之外的条目级别。
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");

/// <summary>
/// 使用文档构建器插入 TC 字段。
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### 也可以看看

* class [FieldTC](../)
* 命名空间 [Aspose.Words.Fields](../../fieldtc/)
* 部件 [Aspose.Words](../../../)


