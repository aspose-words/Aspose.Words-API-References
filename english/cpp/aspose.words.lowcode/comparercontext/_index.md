---
title: Aspose::Words::LowCode::ComparerContext class
linktitle: ComparerContext
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::ComparerContext class. Document comparer context in C++.'
type: docs
weight: 550
url: /cpp/aspose.words.lowcode/comparercontext/
---
## ComparerContext class


[Document](../../aspose.words/document/) comparer context.

```cpp
class ComparerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Methods

| Method | Description |
| --- | --- |
| [ComparerContext](./comparercontext/)() |  |
| [get_AcceptRevisions](./get_acceptrevisions/)() const | Indicates whether to accept revisions in the documents before comparing them. If the compared documents contain revisions and this flag is set to false, the processor will reject revisions. Default is **true**. |
| [get_Author](./get_author/)() const | The author to be assigned to revisions created during document comparison. |
| [get_CompareOptions](./get_compareoptions/)() const | Options used upon comparing documents. |
| [get_DateTime](./get_datetime/)() const | The date and time assigned to revisions created during document comparison. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | [Font](../../aspose.words/font/) settings used by the processor. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | [Document](../../aspose.words/document/) layout options used by the processor. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Warning callback used by the processor. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_AcceptRevisions](./set_acceptrevisions/)(bool) | Indicates whether to accept revisions in the documents before comparing them. If the compared documents contain revisions and this flag is set to false, the processor will reject revisions. Default is **true**. |
| [set_Author](./set_author/)(const System::String\&) | The author to be assigned to revisions created during document comparison. |
| [set_DateTime](./set_datetime/)(System::DateTime) | The date and time assigned to revisions created during document comparison. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | [Font](../../aspose.words/font/) settings used by the processor. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Warning callback used by the processor. |
| static [Type](./type/)() |  |
## See Also

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
