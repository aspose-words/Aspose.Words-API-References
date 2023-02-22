---
title: FieldRD.IsPathRelative
second_title: Aspose.Words for .NET API 参考
description: FieldRD 财产. 获取或设置路径是否相对于当前文档
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldrd/ispathrelative/
---
## FieldRD.IsPathRelative property

获取或设置路径是否相对于当前文档。

```csharp
public bool IsPathRelative { get; set; }
```

### 例子

显示使用 RD 字段从其他文档中的标题创建目录条目。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用文档构建器插入目录，
// 然后为下一页的目录添加一个条目。
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// 插入一个 RD 字段，该字段在其 FileName 属性中引用另一个本地文件系统文档。
// TOC 现在也将接受引用文档中的所有标题作为其表的条目。
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = "ReferencedDocument.docx";
field.IsPathRelative = true;

Assert.AreEqual(" RD  ReferencedDocument.docx \\f", field.GetFieldCode());

 // 创建 RD 字段引用的文档并插入标题。
// 这个标题将在我们的第一个文档的 TOC 字段中显示为一个条目。
Document referencedDoc = new Document();
DocumentBuilder refDocBuilder = new DocumentBuilder(referencedDoc);
refDocBuilder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
refDocBuilder.Writeln("TOC entry from referenced document");
referencedDoc.Save(ArtifactsDir + "ReferencedDocument.docx");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.RD.docx");
```

### 也可以看看

* class [FieldRD](../)
* 命名空间 [Aspose.Words.Fields](../../fieldrd/)
* 部件 [Aspose.Words](../../../)


