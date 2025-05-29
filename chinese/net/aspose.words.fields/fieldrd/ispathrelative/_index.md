---
title: FieldRD.IsPathRelative
linktitle: IsPathRelative
articleTitle: IsPathRelative
second_title: Aspose.Words for .NET
description: 探索 FieldRD 的 IsPathRelative 属性，轻松管理文档路径。灵活的路径设置简化您的编码，提升效率！
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldrd/ispathrelative/
---
## FieldRD.IsPathRelative property

获取或设置路径是否相对于当前文档。

```csharp
public bool IsPathRelative { get; set; }
```

## 例子

显示使用 RD 字段从其他文档中的标题创建目录条目。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用文档生成器插入目录，
// 然后在下一页为目录添加一个条目。
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// 插入一个 RD 字段，该字段在其 FileName 属性中引用另一个本地文件系统文档。
// TOC 现在还将接受引用文档中的所有标题作为其表格的条目。
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // 创建 RD 字段引用的文档并插入标题。
// 此标题将作为我们第一个文档的 TOC 字段中的条目显示。
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
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
