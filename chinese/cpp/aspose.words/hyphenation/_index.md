---
title: "Aspose::Words::Hyphenation 类"
linktitle: "连字符"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Hyphenation 类。提供用于处理连字符字典的方法。这些字典规定了特定语言的单词可以在何处断字。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 33000
url: /zh/cpp/aspose.words/hyphenation/
---
## Hyphenation class


提供处理断字词典的方法。这些词典规定了特定语言的单词可以在何处断字。要了解更多信息，请访问 [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/) 文档文章。

```cpp
class Hyphenation
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [get_Callback](./get_callback/)() | 获取在构建文档页面布局时用于请求字典的回调接口。这允许延迟加载字典，在处理多语言文档时可能会有用。 |
| static [get_WarningCallback](./get_warningcallback/)() | 在加载连字符模式期间调用，如果检测到可能导致格式保真度损失的问题。 |
| [Hyphenation](./hyphenation/)() |  |
| static [IsDictionaryRegistered](./isdictionaryregistered/)(const System::String\&) | 如果指定语言没有注册字典或注册的是 Null 字典，则返回 **false**，否则返回 **true**。 |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) | 从流中为指定语言注册并加载连字符字典。如果字典无法读取或格式无效，则抛出异常。 |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::String\&) | 从文件为指定语言注册并加载连字符字典。如果字典无法读取或格式无效，则抛出异常。此方法也可用于注册 Null 字典，以防止对同一语言重复调用 [Callback](./get_callback/)。 |
| static [RegisterDictionary](./registerdictionary/)(System::String, std::basic_istream\<CharType, Traits\>\&) |  |
| static [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::IHyphenationCallback\>\&) | 设置在构建文档页面布局时用于请求字典的回调接口。这允许延迟加载字典，在处理多语言文档时可能会有用。 |
| static [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 在加载连字符模式期间调用，如果检测到可能导致格式保真度损失的问题。 |
| static [UnregisterDictionary](./unregisterdictionary/)(const System::String\&) | 为指定语言注销连字符字典。这不同于注册 Null 字典。注销字典后将启用该语言的回调。 |
## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
