---
title: "Aspose::Words::LowCode::ComparerContext 类"
linktitle: "ComparerContext"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::ComparerContext 类。C++ 中的文档比较器上下文。"
type: docs
weight: 550
url: /zh/cpp/aspose.words.lowcode/comparercontext/
---
## ComparerContext class


[Document](../../aspose.words/document/) comparer context.

```cpp
class ComparerContext : public Aspose::Words::LowCode::ProcessorContext
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ComparerContext](./comparercontext/)() |  |
| [get_AcceptRevisions](./get_acceptrevisions/)() const | 指示在比较文档之前是否接受文档中的修订。如果被比较的文档包含修订且此标志设置为 false，处理器将拒绝修订。默认值为 **true**。 |
| [get_Author](./get_author/)() const | 在文档比较期间创建的修订所分配的作者。 |
| [get_CompareOptions](./get_compareoptions/)() const | 比较文档时使用的选项。 |
| [get_DateTime](./get_datetime/)() const | 在文档比较期间创建的修订所分配的日期和时间。 |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | 处理器使用的 [Font](../../aspose.words/font/) 设置。 |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | 处理器使用的 [Document](../../aspose.words/document/) 布局选项。 |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | 处理器使用的警告回调。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_AcceptRevisions](./set_acceptrevisions/)(bool) | 指示在比较文档之前是否接受文档中的修订。如果被比较的文档包含修订且此标志设置为 false，处理器将拒绝修订。默认值为 **true**。 |
| [set_Author](./set_author/)(const System::String\&) | 在文档比较期间创建的修订所分配的作者。 |
| [set_DateTime](./set_datetime/)(System::DateTime) | 在文档比较期间创建的修订所分配的日期和时间。 |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | 处理器使用的 [Font](../../aspose.words/font/) 设置。 |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 处理器使用的警告回调。 |
| static [Type](./type/)() |  |
## 另见

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
