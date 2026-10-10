---
title: "Aspose::Words::LowCode::MailMergerContext class"
linktitle: "MailMergerContext"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::MailMergerContext class. C++ 中的邮件合并上下文。"
type: docs
weight: 875
url: /zh/cpp/aspose.words.lowcode/mailmergercontext/
---
## MailMergerContext class


邮件合并上下文。

```cpp
class MailMergerContext : public Aspose::Words::LowCode::ProcessorContext
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | 处理器使用的 [Font](../../aspose.words/font/) 设置。 |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | 处理器使用的 [Document](../../aspose.words/document/) 布局选项。 |
| [get_MailMergeOptions](./get_mailmergeoptions/)() const | 邮件合并选项。 |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | 处理器使用的警告回调。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergerContext](./mailmergercontext/)() |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | 处理器使用的 [Font](../../aspose.words/font/) 设置。 |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 处理器使用的警告回调。 |
| [SetRegionsDataSource](./setregionsdatasource/)(const System::SharedPtr\<System::Data::DataTable\>\&) | 设置用于执行带区域的邮件合并的数据源。 |
| [SetRegionsDataSource](./setregionsdatasource/)(const System::SharedPtr\<System::Data::DataSet\>\&) | 设置用于执行带区域的邮件合并的数据源。 |
| [SetSimpleDataSource](./setsimpledatasource/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | 设置用于执行简单邮件合并的数据源。 |
| [SetSimpleDataSource](./setsimpledatasource/)(const System::SharedPtr\<System::Data::DataRow\>\&) | 设置用于执行简单邮件合并的数据源。 |
| [SetSimpleDataSource](./setsimpledatasource/)(const System::SharedPtr\<System::Data::DataTable\>\&) | 设置用于执行简单邮件合并的数据源。 |
| static [Type](./type/)() |  |
## 另见

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
