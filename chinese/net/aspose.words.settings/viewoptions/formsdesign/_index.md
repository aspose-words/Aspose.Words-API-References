---
title: ViewOptions.FormsDesign
linktitle: FormsDesign
articleTitle: FormsDesign
second_title: Aspose.Words for .NET
description: 了解 ViewOptions FormsDesign 如何通过切换表单设计模式实现无缝编辑和自定义，从而增强您的文档体验。
type: docs
weight: 30
url: /zh/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

指定文档是否处于表单设计模式。

```csharp
public bool FormsDesign { get; set; }
```

## 评论

目前仅适用于 WordML 格式的文档。

## 例子

显示如何启用/禁用表单设计模式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 将“FormsDesign”属性设置为“false”以保持表单设计模式处于禁用状态。
// 将“FormsDesign”属性设置为“true”以启用表单设计模式。
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### 也可以看看

* class [ViewOptions](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
