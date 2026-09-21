---
title: "Aspose::Words::LowCode::ComparerContext klass"
linktitle: "ComparerContext"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::ComparerContext klass. Dokumentjämförelsesammanhang i C++."
type: docs
weight: 550
url: /sv/cpp/aspose.words.lowcode/comparercontext/
---
## ComparerContext class


[Document](../../aspose.words/document/) comparer context.

```cpp
class ComparerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ComparerContext](./comparercontext/)() |  |
| [get_AcceptRevisions](./get_acceptrevisions/)() const | Indikerar om revisioner i dokumenten ska accepteras innan de jämförs. Om de jämförda dokumenten innehåller revisioner och denna flagga är satt till false, kommer processorn att avvisa revisioner. Standard är **true**. |
| [get_Author](./get_author/)() const | Författaren som ska tilldelas revisioner som skapats under dokumentjämförelse. |
| [get_CompareOptions](./get_compareoptions/)() const | Alternativ som används vid jämförelse av dokument. |
| [get_DateTime](./get_datetime/)() const | Datum och tid som tilldelas revisioner som skapats under dokumentjämförelse. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | [Font](../../aspose.words/font/) inställningar som används av processorn. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | [Document](../../aspose.words/document/) layoutalternativ som används av processorn. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Varningscallback som används av processorn. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_AcceptRevisions](./set_acceptrevisions/)(bool) | Indikerar om revisioner i dokumenten ska accepteras innan de jämförs. Om de jämförda dokumenten innehåller revisioner och denna flagga är satt till false, kommer processorn att avvisa revisioner. Standard är **true**. |
| [set_Author](./set_author/)(const System::String\&) | Författaren som ska tilldelas revisioner som skapats under dokumentjämförelse. |
| [set_DateTime](./set_datetime/)(System::DateTime) | Datum och tid som tilldelas revisioner som skapats under dokumentjämförelse. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | [Font](../../aspose.words/font/) inställningar som används av processorn. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Varningscallback som används av processorn. |
| static [Type](./type/)() |  |
## Se även

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
