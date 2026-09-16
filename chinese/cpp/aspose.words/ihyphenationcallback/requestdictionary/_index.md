---
title: "Aspose::Words::IHyphenationCallback::RequestDictionary 方法"
linktitle: "RequestDictionary"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IHyphenationCallback::RequestDictionary 方法。通知应用程序未找到指定语言的断字词典，可能需要进行注册。实现应查找词典并使用 RegisterDictionary() 方法进行注册。如果指定语言的词典不可用，实现可以在 C++ 中通过使用带 null 值的 RegisterDictionary() 来停止对同一语言的后续调用。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback::RequestDictionary method


通知应用程序未找到指定语言的断字词典，可能需要注册。实现应查找词典并使用 [RegisterDictionary()](../) 方法进行注册。如果指定语言的词典不可用，实现可以使用带 **null** 值的 [RegisterDictionary()](../) 来停止对同一语言的后续调用。

```cpp
virtual void Aspose::Words::IHyphenationCallback::RequestDictionary(System::String language)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 语言 | System::String | 语言名称，例如 "en-US"。有关 "culture name" 请参阅 .NET 文档，详细信息请参阅 RFC 4646。 |

## 另见

* Interface [IHyphenationCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
