---
title: "Aspose::Words::Layout namespace"
linktitle: "Aspose::Words::Layout"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout 命名空间。Aspose.Words.Layout 命名空间提供类，允许在文档格式化为页面时访问信息，例如特定文档元素位于哪一页以及在页面上的位置，适用于 C++。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.layout/
---

该 **Aspose.Words.Layout** 命名空间提供允许在文档分页格式化时获取特定文档元素所在页码及页内位置等信息的类。

## 类

| 类 | 描述 |
| --- | --- |
| [LayoutCollector](./layoutcollector/) | 此类允许计算文档节点的页码。欲了解更多信息，请访问 [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) 文档文章。 |
| [LayoutEnumerator](./layoutenumerator/) | 枚举文档的页面布局实体。您可以使用此类遍历页面布局模型。可用属性包括实体的类型、几何形状、文本以及渲染所在的页索引，还包括整体结构和关系。结合使用 [GetEntity()](../) 和 [Current](./layoutenumerator/get_current/) 可移动到对应文档节点的实体。欲了解更多信息，请访问 [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) 文档文章。 |
| [LayoutOptions](./layoutoptions/) | 保存允许控制文档布局过程的选项。欲了解更多信息，请访问 [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) 文档文章。 |
| [PageLayoutCallbackArgs](./pagelayoutcallbackargs/) | 传递给 [Notify()](./ipagelayoutcallback/notify/) 的参数。欲了解更多信息，请访问 [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) 文档文章。 |
| [RevisionOptions](./revisionoptions/) | 允许控制布局过程中文档修订的处理方式。欲了解更多信息，请访问 [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) 文档文章。 |
## 接口

| 接口 | 描述 |
| --- | --- |
| [IPageLayoutCallback](./ipagelayoutcallback/) | 如果您希望在页面布局模型的构建和渲染期间调用自定义方法，请实现此接口。 |
## Enums

| 枚举 | 描述 |
| --- | --- |
| [CommentDisplayMode](./commentdisplaymode/) | 指定文档批注的渲染模式。 |
| [ContinuousSectionRestart](./continuoussectionrestart/) | 表示在连续节中重新开始页码时计算页码的不同行为。 |
| [LayoutEntityType](./layoutentitytype/) | 布局实体的类型。 |
| [PageLayoutEvent](./pagelayoutevent/) | 在页面布局模型构建和渲染期间触发的事件代码。页面布局模型分两步构建。第一步，"转换步骤"，此时页面布局提取文档内容并创建对象图。第二步，"重排步骤"，此时结构被拆分、合并并排列成页面。根据触发构建的操作，页面布局模型可能会或可能不会进一步渲染为固定页面格式。例如，计算文档页数或更新字段不需要渲染，而导出为 PDF 则需要。 |
| [RevisionColor](./revisioncolor/) | 允许指定文档修订的颜色。 |
| [RevisionTextEffect](./revisiontexteffect/) | 允许为文档文本的修订指定装饰效果。 |
| [ShowInBalloons](./showinballoons/) | 指定哪些修订以气泡形式渲染。 |
