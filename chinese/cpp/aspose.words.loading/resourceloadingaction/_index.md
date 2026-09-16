---
title: "Aspose::Words::Loading::ResourceLoadingAction 枚举"
linktitle: "ResourceLoadingAction"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::ResourceLoadingAction 枚举。指定资源加载的模式。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enum


指定资源加载模式。欲了解更多，请访问 [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) 文档文章。

```cpp
enum class ResourceLoadingAction
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Default | 0 | Aspose.Words 将照常加载此资源。 |
| 跳过 | 1 | Aspose.Words 将跳过此资源的加载。仅会为图像存储没有数据的链接，HTML 格式下 CSS 样式表将被忽略。 |
| UserProvided | 2 | Aspose.Words 将使用用户在 [SetData()](../) 中提供的字节数组作为资源数据。 |

## 另见

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
