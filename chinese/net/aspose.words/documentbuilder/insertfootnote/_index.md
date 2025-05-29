---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder InsertFootnote 方法轻松增强您的文档 - 轻松添加脚注或尾注以获得更好的清晰度和专业性。
type: docs
weight: 340
url: /zh/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string*) {#insertfootnote}

在文档中插入脚注或尾注。

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| footnoteType | FootnoteType | 指定是否插入脚注或尾注。 |
| footnoteText | String | 指定脚注的文本。 |

### 返回值

返回刚刚创建的脚注对象。

## 例子

展示如何使用脚注和尾注引用文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一些文本并用脚注标记，IsAuto 属性默认设置为“true”，
// 因此正文中看到的标记将自动编号为“1”，
// 并且脚注将出现在页面底部。
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// 插入更多文本并使用带有自定义引用标记的尾注进行标记，
// 将代替数字“2”并将“IsAuto”设置为 false。
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// 脚注总是出现在引用文本的底部，
// 因此此分页符不会影响脚注。
// 另一方面，尾注始终位于文档末尾
// 这样，此分页符就会将尾注推到下一页。
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### 也可以看看

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string, string*) {#insertfootnote_1}

在文档中插入脚注或尾注。

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| footnoteType | FootnoteType | 指定是否插入脚注或尾注。 |
| footnoteText | String | 指定脚注的文本。 |
| referenceMark | String | 指定脚注的自定义引用标记。 |

### 返回值

返回刚刚创建的脚注对象。

## 例子

展示如何使用脚注和尾注引用文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一些文本并用脚注标记，IsAuto 属性默认设置为“true”，
// 因此正文中看到的标记将自动编号为“1”，
// 并且脚注将出现在页面底部。
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// 插入更多文本并使用带有自定义引用标记的尾注进行标记，
// 将代替数字“2”并将“IsAuto”设置为 false。
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// 脚注总是出现在引用文本的底部，
// 因此此分页符不会影响脚注。
// 另一方面，尾注始终位于文档末尾
// 这样，此分页符就会将尾注推到下一页。
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### 也可以看看

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
