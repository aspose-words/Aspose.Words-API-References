---
title: Document.AppendDocument
linktitle: AppendDocument
articleTitle: AppendDocument
second_title: 用于 .NET 的 Aspose.Words
description: Document AppendDocument 方法. 将指定的文档附加到该文档的末尾 在 C#.
type: docs
weight: 530
url: /zh/net/aspose.words/document/appenddocument/
---
## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/)*) {#appenddocument}

将指定的文档附加到该文档的末尾。

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | Document | 要附加的文档。 |
| importFormatMode | ImportFormatMode | 指定如何合并有冲突的样式格式。 |

## 例子

演示如何将文档附加到另一个文档的末尾。

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// 将源文档附加到目标文档，同时保留其格式，
// 然后将源文档保存到本地文件系统。
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

演示如何将文件夹中的所有文档附加到模板文档的末尾。

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");

// 使用 .doc 扩展名附加所有未加密的文档
// 从我们的本地文件系统目录到基础文档。
List<string> docFiles = Directory.GetFiles(MyDir, "*.doc").Where(item => item.EndsWith(".doc")).ToList();
foreach (string fileName in docFiles)
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(fileName);
    if (info.IsEncrypted)
        continue;

    Document srcDoc = new Document(fileName);
    dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);
}

dstDoc.Save(ArtifactsDir + "Document.AppendAllDocumentsInFolder.doc");
```

### 也可以看看

* enum [ImportFormatMode](../../importformatmode/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#appenddocument_1}

将指定的文档附加到该文档的末尾。

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcDoc | Document | 要附加的文档。 |
| importFormatMode | ImportFormatMode | 指定如何合并有冲突的样式格式。 |
| importFormatOptions | ImportFormatOptions | 允许指定影响结果文档格式的选项。 |

## 例子

演示如何在将文档的克隆附加到自身时管理列表样式冲突。

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// 如果列表样式冲突，应用源文档的列表格式。
// 将“KeepSourceNumbering”属性设置为“false”以不将任何列表编号导入目标文档。
// 将“KeepSourceNumbering”属性设置为“true”导入所有冲突
// 列出与源文档中相同外观的样式编号。
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.SectionBreakNewPage);

ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;
builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.UpdateListLabels();
```

显示如何在插入文档时管理列表样式冲突。

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.InsertBreak(BreakType.ParagraphBreak);

dstDoc.Lists.Add(ListTemplate.NumberDefault);
Aspose.Words.Lists.List list = dstDoc.Lists[0];

builder.ListFormat.List = list;

for (int i = 1; i <= 15; i++)
    builder.Write($"List Item {i}\n");

Document attachDoc = (Document)dstDoc.Clone(true);

// 如果列表样式冲突，应用源文档的列表格式。
// 将“KeepSourceNumbering”属性设置为“false”以不将任何列表编号导入目标文档。
// 将“KeepSourceNumbering”属性设置为“true”导入所有冲突
// 列出与源文档中相同外观的样式编号。
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

显示如何在附加文档时管理列表样式冲突。

```csharp
// 加载带有自定义样式文本的文档并克隆它。
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// 我们现在有两个文档，每个文档都有一个相同的样式，名为“CustomStyle”。
// 更改其中一种样式的文本颜色以将其与另一种分开。
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// 如果列表样式冲突，应用源文档的列表格式。
// 将“KeepSourceNumbering”属性设置为“false”以不将任何列表编号导入目标文档。
// 将“KeepSourceNumbering”属性设置为“true”导入所有冲突
// 列出与源文档中相同外观的样式编号。
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// 连接两个具有不同样式但名称相同的文档会导致样式冲突。
// 我们可以在附加文档时指定导入格式模式来解决这种冲突。
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepDifferentStyles, options);
dstDoc.UpdateListLabels();

dstDoc.Save(ArtifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

### 也可以看看

* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
