---
title: "Aspose::Words::IHyphenationCallback 接口"
linktitle: "IHyphenationCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IHyphenationCallback 接口。由能够在 C++ 中注册断字词典的类实现。"
type: docs
weight: 78000
url: /zh/cpp/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface


由能够注册断字字典的类实现。

```cpp
class IHyphenationCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RequestDictionary](./requestdictionary/)(System::String) | 通知应用程序未找到指定语言的断字词典，可能需要注册。实现应查找词典并使用 [RegisterDictionary()](../) 方法进行注册。如果指定语言的词典不可用，实现可以使用带 **null** 值的 [RegisterDictionary()](../) 来停止对同一语言的后续调用。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
