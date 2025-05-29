---
title: Document.CopyStylesFromTemplate
linktitle: CopyStylesFromTemplate
articleTitle: CopyStylesFromTemplate
second_title: Aspose.Words for .NET
description: 使用 CopyStylesFromTemplate 方法轻松地将样式从您选择的模板复制到任何文档，从而增强您的工作流程和文档一致性。
type: docs
weight: 610
url: /zh/net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(*string*) {#copystylesfromtemplate_1}

将样式从指定的模板复制到文档。

```csharp
public void CopyStylesFromTemplate(string template)
```

## 评论

将样式从模板复制到文档时， 文档中同名的样式会被重新定义，以匹配模板中的样式描述。 模板中特有的样式会被复制到文档中。文档中特有的样式保持不变。

## 例子

展示如何将样式从一个文档复制到另一个文档。

```csharp
// 创建一个文档，然后添加我们将复制到另一个文档的样式。
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// 创建一个我们将复制样式的文档。
Document target = new Document();

// 从模板文档中创建与样式同名的样式并将其添加到目标文档。
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// 有两种方式可以调用该方法将所有样式从一个文档复制到另一个文档。
// 1 - 传递模板文档对象：
target.CopyStylesFromTemplate(template);

// 复制样式会将模板文档中的所有样式添加到目标
// 并覆盖具有相同名称的现有样式。
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - 传递模板文档的本地系统文件名：
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(*[Document](../)*) {#copystylesfromtemplate}

将样式从指定的模板复制到文档。

```csharp
public void CopyStylesFromTemplate(Document template)
```

## 评论

将样式从模板复制到文档时， 文档中同名的样式会被重新定义，以匹配模板中的样式描述。 模板中特有的样式会被复制到文档中。文档中特有的样式保持不变。

## 例子

展示如何通过文档将样式从模板复制到文档。

```csharp
Document template = new Document(MyDir + "Rendering.docx");
Document target = new Document(MyDir + "Document.docx");

target.CopyStylesFromTemplate(template);
```

展示如何将样式从一个文档复制到另一个文档。

```csharp
// 创建一个文档，然后添加我们将复制到另一个文档的样式。
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// 创建一个我们将复制样式的文档。
Document target = new Document();

// 从模板文档中创建与样式同名的样式并将其添加到目标文档。
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// 有两种方式可以调用该方法将所有样式从一个文档复制到另一个文档。
// 1 - 传递模板文档对象：
target.CopyStylesFromTemplate(template);

// 复制样式会将模板文档中的所有样式添加到目标
// 并覆盖具有相同名称的现有样式。
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - 传递模板文档的本地系统文件名：
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
