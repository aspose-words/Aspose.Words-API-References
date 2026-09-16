---
title: "Aspose::Words::Loading 命名空间"
linktitle: "Aspose::Words::Loading"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading 命名空间。Aspose.Words.Loading 命名空间提供类和枚举，允许在 C++ 中加载文档时指定附加选项。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.loading/
---

该 **Aspose.Words.Loading** 命名空间提供允许在加载文档时指定附加选项的类和枚举。

## 类

| 类 | 描述 |
| --- | --- |
| [ChmLoadOptions](./chmloadoptions/) | 在将 CHM 文档加载到 [Document](../aspose.words/document/) 对象时，允许指定附加选项。欲了解更多，请访问[Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/)文档文章。 |
| [DocumentLoadingArgs](./documentloadingargs/) | 传递给 [Notify()](./idocumentloadingcallback/notify/) 的参数。欲了解更多，请访问[Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/)文档文章。 |
| [HtmlLoadOptions](./htmlloadoptions/) | 在将 HTML 文档加载到 [Document](../aspose.words/document/) 对象时，允许指定附加选项。欲了解更多，请访问[Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/)文档文章。 |
| [LanguagePreferences](./languagepreferences/) | 允许设置语言首选项。欲了解更多，请访问[Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/)文档文章。 |
| [LoadOptions](./loadoptions/) | 在将文档加载到 [Document](../aspose.words/document/) 对象时，允许指定附加选项（例如密码或基础 URI）。欲了解更多，请访问[Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/)文档文章。 |
| [MarkdownLoadOptions](./markdownloadoptions/) | 在将 [Markdown](../aspose.words/loadformat/) 文档加载到 [Document](../aspose.words/document/) 对象时，允许指定附加选项。 |
| [PdfLoadOptions](./pdfloadoptions/) | 允许在将 Pdf 文档加载到 [Document](../aspose.words/document/) 对象时指定其他选项。欲了解更多，请访问 [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) 文档文章。 |
| [ResourceLoadingArgs](./resourceloadingargs/) | 为 [ResourceLoading()](./iresourceloadingcallback/resourceloading/) 方法提供数据。 |
| [RtfLoadOptions](./rtfloadoptions/) | 允许在将 [Rtf](../aspose.words/loadformat/) 文档加载到 [Document](../aspose.words/document/) 对象时指定其他选项。欲了解更多，请访问 [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) 文档文章。 |
| [TxtLoadOptions](./txtloadoptions/) | 允许在将 [Text](../aspose.words/loadformat/) 文档加载到 [Document](../aspose.words/document/) 对象时指定其他选项。欲了解更多，请访问 [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) 文档文章。 |
## 接口

| 接口 | 描述 |
| --- | --- |
| [IDocumentLoadingCallback](./idocumentloadingcallback/) | 如果您希望在加载文档期间调用自己的自定义方法，请实现此接口。 |
| [IResourceLoadingCallback](./iresourceloadingcallback/) | 如果您想控制 Aspose.Words 在导入文档并使用 [DocumentBuilder](../aspose.words/documentbuilder/) 插入图像时加载外部资源的方式，请实现此接口。 |
## Enums

| 枚举 | 描述 |
| --- | --- |
| [BlockImportMode](./blockimportmode/) | 指定块级元素的属性如何从基于 HTML 的文档中导入。 |
| [DocumentDirection](./documentdirection/) | 允许指定文档中文本的流向。 |
| [DocumentRecoveryMode](./documentrecoverymode/) | 指定文档在加载期间遇到错误时可用的恢复选项。 |
| [EditingLanguage](./editinglanguage/) | 指定编辑语言。 |
| [HtmlControlType](./htmlcontroltype/) | 表示从 HTML 导入的 <input> 和 <select> 元素的文档节点类型。 |
| [ResourceLoadingAction](./resourceloadingaction/) | 指定资源加载模式。欲了解更多，请访问 [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) 文档文章。 |
| [ResourceType](./resourcetype/) | 已加载资源的类型。 |
| [TxtLeadingSpacesOptions](./txtleadingspacesoptions/) | 指定从 [Text](../aspose.words/loadformat/) 文件导入时对前导空格的处理可用选项。 |
| [TxtTrailingSpacesOptions](./txttrailingspacesoptions/) | 指定从 [Text](../aspose.words/loadformat/) 文件导入时对尾随空格的处理可用选项。 |
