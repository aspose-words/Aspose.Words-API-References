---
title: IDocumentProcessorPlugin.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words for .NET
description: 使用 IDocumentProcessorPlugin Save 方法轻松保存文档，确保通过可定制的保存选项实现最佳输出，满足您的需求。
type: docs
weight: 30
url: /zh/net/aspose.words/idocumentprocessorplugin/save/
---
## IDocumentProcessorPlugin.Save method

保存由加载的文档[`Load`](../load/)方法使用指定的保存选项将数据保存到输出流。

```csharp
public void Save(Stream outputStream, SaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | Stream | 输出流。 |
| saveOptions | SaveOptions | 保存选项。 |

## 评论

如果指定的输出格式是图像，则只有第一页图像保存到输出流。 如果插件本身不支持指定的保存格式（需要加载到[`Document`](../../document/)), 方法抛出异常。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* interface [IDocumentProcessorPlugin](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
