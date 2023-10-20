---
title: FieldTC.Text
linktitle: Text
articleTitle: Text
second_title: 用于 .NET 的 Aspose.Words
description: FieldTC Text 财产. 获取或设置条目的文本 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldtc/text/
---
## FieldTC.Text property

获取或设置条目的文本。

```csharp
public string Text { get; set; }
```

## 例子

展示如何插入 TOC 字段，以及过滤哪些 TC 字段最终作为条目。

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入一个TOC字段，这会将所有TC字段编译成目录。
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // 配置该字段仅拾取“A”类型的 TC 条目，以及 1 到 3 之间的条目级别。
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // 这两个条目将出现在表中。
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // 该条目将从表中省略，因为它的类型与“A”不同。
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // 该条目将从表中省略，因为它的条目级别超出了 1-3 范围。
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// 使用文档生成器插入 TC 字段。
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
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
