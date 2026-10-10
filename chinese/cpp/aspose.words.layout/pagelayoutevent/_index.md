---
title: "Aspose::Words::Layout::PageLayoutEvent 枚举"
linktitle: "PageLayoutEvent"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::PageLayoutEvent 枚举。页面布局模型构建和渲染期间触发的事件代码。页面布局模型分两步构建。第一步，“conversion step”，此时页面布局提取文档内容并创建对象图。第二步，“reflow step”，此时结构被拆分、合并并排列成页面。根据触发构建的操作，页面布局模型可能会也可能不会进一步渲染为固定页面格式。例如，计算文档页数或更新字段不需要渲染，而导出为 PDF 在 C++ 中则需要渲染。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enum


在页面布局模型构建和渲染期间触发的事件代码。页面布局模型分两步构建。第一步，"转换步骤"，此时页面布局提取文档内容并创建对象图。第二步，"重排步骤"，此时结构被拆分、合并并排列成页面。根据触发构建的操作，页面布局模型可能会或可能不会进一步渲染为固定页面格式。例如，计算文档页数或更新字段不需要渲染，而导出为 PDF 则需要。

```cpp
enum class PageLayoutEvent
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 默认值。 |
| WatchDog | 1 | 对应代码中经常访问且适合中止过程的检查点。在 [Notify()](../ipagelayoutcallback/notify/) 内部抛出自定义异常以中止过程。您可以在处理任何回调事件时抛出以中止过程。请注意，如果过程被中止，页面布局模型将处于未定义状态。但如果在完整页面的 reflow 期间中止过程，仍应能够使用该页面结束前的布局模型。 |
| BuildStarted | 2 | 页面布局的构建已开始。仅触发一次。这是首次在调用 [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) 时发生的事件。 |
| BuildFinished | 3 | 页面布局的构建已完成。仅触发一次。这是最后一次在调用 [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) 时发生的事件。 |
| ConversionStarted | 4 | 文档模型转换为页面布局已开始。仅触发一次。当布局模型开始提取文档内容时发生此事件。 |
| ConversionFinished | 5 | 文档模型转换为页面布局已完成。仅触发一次。当布局模型停止提取文档内容时发生此事件。 |
| ReflowStarted | 6 | 页面布局的重排已开始。仅触发一次。当布局模型开始对文档内容进行重排时发生此事件。 |
| ReflowFinished | 7 | 页面布局的重排已完成。仅触发一次。当布局模型停止对文档内容进行重排时发生此事件。 |
| PartReflowStarted | 8 | 页面的重排已开始。请注意，页面可能会多次重排，且重排可能在完成之前重新启动。 |
| PartReflowFinished | 9 | 页面的重排已完成。请注意，页面可能会多次重排，且重排可能在完成之前重新启动。 |
| PartRenderingStarted | 10 | 页面的[Rendering](../../aspose.words.rendering/)已开始。此事件每页触发一次。 |
| PartRenderingFinished | 11 | 页面的[Rendering](../../aspose.words.rendering/)已完成。此事件每页触发一次。 |

## 另见

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
