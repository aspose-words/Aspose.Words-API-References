---
title: Document.CopyStylesFromTemplate
second_title: Aspose.Words for .NET API 参考
description: Document 方法. 将样式从指定模板复制到文档
type: docs
weight: 550
url: /zh/net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(string) {#copystylesfromtemplate_1}

将样式从指定模板复制到文档。

```csharp
public void CopyStylesFromTemplate(string template)
```

### 评论

当样式从模板复制到文档时， 文档中类似命名的样式被重新定义以匹配模板中的样式描述。 模板中的唯一样式被复制到文档中。文档中的独特样式保持不变。

### 例子

演示如何将样式从一个文档复制到另一个文档。

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

// 创建一个将样式复制到的文档。
Document target = new Document();

// 创建一个与模板文档中的样式同名的样式，并将其添加到目标文档中。
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// 调用方法将所有样式从一个文档复制到另一个文档有两种方式。
// 1 - 传递模板文档对象：
target.CopyStylesFromTemplate(template);

// 复制样式将模板文档中的所有样式添加到目标
// 并覆盖现有的同名样式。
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - 传递模板文档的本地系统文件名：
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(Document) {#copystylesfromtemplate}

将样式从指定模板复制到文档。

```csharp
public void CopyStylesFromTemplate(Document template)
```

### 评论

当样式从模板复制到文档时， 文档中类似命名的样式被重新定义以匹配模板中的样式描述。 模板中的唯一样式被复制到文档中。文档中的独特样式保持不变。

### 例子

展示如何通过 Document 将样式从模板复制到文档。

```csharp
Document template = new Document(MyDir + "Rendering.docx");
Document target = new Document(MyDir + "Document.docx");

target.CopyStylesFromTemplate(template);
```

演示如何将样式从一个文档复制到另一个文档。

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

// 创建一个将样式复制到的文档。
Document target = new Document();

// 创建一个与模板文档中的样式同名的样式，并将其添加到目标文档中。
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// 调用方法将所有样式从一个文档复制到另一个文档有两种方式。
// 1 - 传递模板文档对象：
target.CopyStylesFromTemplate(template);

// 复制样式将模板文档中的所有样式添加到目标
// 并覆盖现有的同名样式。
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - 传递模板文档的本地系统文件名：
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


