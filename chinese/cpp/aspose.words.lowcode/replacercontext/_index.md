---
title: "Aspose::Words::LowCode::ReplacerContext class"
linktitle: "ReplacerContext"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::ReplacerContext 类。C++ 中的查找/替换操作上下文。"
type: docs
weight: 1292
url: /zh/cpp/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class


查找/替换操作上下文。

```cpp
class ReplacerContext : public Aspose::Words::LowCode::ProcessorContext
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_FindReplaceOptions](./get_findreplaceoptions/)() const | 查找/替换选项。 |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | 处理器使用的 [Font](../../aspose.words/font/) 设置。 |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | 处理器使用的 [Document](../../aspose.words/document/) 布局选项。 |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | 处理器使用的警告回调。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [ReplacerContext](./replacercontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | 处理器使用的 [Font](../../aspose.words/font/) 设置。 |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 处理器使用的警告回调。 |
| [SetReplacement](./setreplacement/)(const System::String\&, const System::String\&) | 设置查找/替换操作使用的模式和替换内容。 |
| [SetReplacement](./setreplacement/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | 设置查找/替换操作使用的模式和替换内容。 |
| static [Type](./type/)() |  |
## 另见

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
