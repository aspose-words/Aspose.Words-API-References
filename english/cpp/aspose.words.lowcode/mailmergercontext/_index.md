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
class MailMergerContext : public ProcessorContext
```

## Methods

| Method | Description |
| --- | --- |
| [MailMergerContext](./mailmergercontext/)() |  |
| [SetRegionsDataSource](./setregionsdatasource/)(const System::SharedPtr\<System::Data::DataSet\> \&) | Sets data source used to execute mail merge with regions. |
| [SetRegionsDataSource](./setregionsdatasource/)(const System::SharedPtr\<System::Data::DataTable\> \&) | Sets data source used to execute mail merge with regions. |
| [SetSimpleDataSource](./setsimpledatasource/)(const System::ArrayPtr\<System::String\> \&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\> \&) | Sets data source used to execute simple mail merge. |
| [SetSimpleDataSource](./setsimpledatasource/)(const System::SharedPtr\<System::Data::DataRow\> \&) | Sets data source used to execute simple mail merge. |
| [SetSimpleDataSource](./setsimpledatasource/)(const System::SharedPtr\<System::Data::DataTable\> \&) | Sets data source used to execute simple mail merge. |
| [get_MailMergeOptions](./get_mailmergeoptions/)() const | Mail merge options. |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Font settings used by the processor. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Document layout options used by the processor. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Warning callback used by the processor. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\> \&) | Font settings used by the processor. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\> \&) | Warning callback used by the processor. |
## See Also

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
