---
title: FieldTC.TypeIdentifier
linktitle: TypeIdentifier
articleTitle: TypeIdentifier
second_title: Aspose.Words for .NET
description: 探索 FieldTC 的 TypeIdentifier 属性。使用此多功能功能轻松管理字段类型标识符，增强数据组织能力并提高效率。
type: docs
weight: 50
url: /zh/net/aspose.words.fields/fieldtc/typeidentifier/
---
## FieldTC.TypeIdentifier property

获取或设置此字段的类型标识符（通常为字母）。

```csharp
public string TypeIdentifier { get; set; }
```

## 例子

显示如何插入 TOC 字段，并过滤最终作为条目的 TC 字段。

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入一个 TOC 字段，它将把所有 TC 字段编译成一个目录。
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // 配置该字段仅选取“A”类型且条目级别在 1 到 3 之间的 TC 条目。
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
