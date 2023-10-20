---
title: DocumentBuilder.InsertDocument
linktitle: InsertDocument
articleTitle: InsertDocument
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder InsertDocument 方法. 在光标位置插入文档 在 C#.
type: docs
weight: 310
url: /zh/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/)*) {#insertdocument}

在光标位置插入文档。

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | Document | 用于插入的源文档。 |
| importFormatMode | ImportFormatMode | 指定如何合并冲突的样式格式。 |

### 返回值

插入内容的第一个节点。

## 评论

此方法模仿 MS Word 行为，就好像按下了 CTRL+'A'（选择所有内容）， 然后在一个文档内按 CTRL+'C'（将所选内容复制到缓冲区中） ，然后按 CTRL+'V'（从文档中插入内容）缓冲区）在另一个文档中。

## 例子

演示如何将一个文档插入到另一个文档中。

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### 也可以看看

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#insertdocument_1}

在光标位置插入文档。

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | Document | 用于插入的源文档。 |
| importFormatMode | ImportFormatMode | 指定如何合并冲突的样式格式。 |
| importFormatOptions | ImportFormatOptions | 允许指定影响结果文档格式的选项。 |

### 返回值

插入内容的第一个节点。

## 评论

此方法模仿 MS Word 行为，就好像按下了 CTRL+'A'（选择所有内容）， 然后在一个文档内按 CTRL+'C'（将所选内容复制到缓冲区中） ，然后按 CTRL+'V'（从文档中插入内容）缓冲区）在另一个文档中。

## 例子

演示如何在插入文档时解决重复样式。

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// 克隆文档并编辑克隆的“MyStyle”样式，使其颜色与原始颜色不同。
// 如果我们将克隆插入到原始文档中，两个同名的样式会产生冲突。
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// 当我们启用SmartStyleBehavior并使用KeepSourceFormatting导入格式模式时，
// Aspose.Words 将通过转换源文档样式来解决样式冲突。
// 与目标样式同名的直接段落属性。
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### 也可以看看

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
