---
title: Aspose::Words::LowCode::MailMergerContext class
linktitle: MailMergerContext
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::MailMergerContext class. Mail merge context in C++.'
type: docs
weight: 875
url: /cpp/aspose.words.lowcode/mailmergercontext/
---
## MailMergerContext class


Mail merge context.

```cpp
class MailMergerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Methods

| Method | Description |
| --- | --- |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | [Font](../../aspose.words/font/) settings used by the processor. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | [Document](../../aspose.words/document/) layout options used by the processor. |
| [get_MailMergeOptions](./get_mailmergeoptions/)() const | Mail merge options. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Warning callback used by the processor. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergerContext](./mailmergercontext/)() |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | [Font](../../aspose.words/font/) settings used by the processor. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Warning callback used by the processor. |
| [SetRegionsDataSource](./setregionsdatasource/)(const System::SharedPtr\<System::Data::DataTable\>\&) | Sets data source used to execute mail merge with regions. |
| [SetRegionsDataSource](./setregionsdatasource/)(const System::SharedPtr\<System::Data::DataSet\>\&) | Sets data source used to execute mail merge with regions. |
| [SetSimpleDataSource](./setsimpledatasource/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | Sets data source used to execute simple mail merge. |
| [SetSimpleDataSource](./setsimpledatasource/)(const System::SharedPtr\<System::Data::DataRow\>\&) | Sets data source used to execute simple mail merge. |
| [SetSimpleDataSource](./setsimpledatasource/)(const System::SharedPtr\<System::Data::DataTable\>\&) | Sets data source used to execute simple mail merge. |
| static [Type](./type/)() |  |
## See Also

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
