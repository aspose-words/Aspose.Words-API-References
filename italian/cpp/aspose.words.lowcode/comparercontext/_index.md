---
title: "Classe Aspose::Words::LowCode::ComparerContext"
linktitle: "ComparerContext"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::LowCode::ComparerContext. Contesto di confronto dei documenti in C++."
type: docs
weight: 550
url: /it/cpp/aspose.words.lowcode/comparercontext/
---
## ComparerContext class


[Document](../../aspose.words/document/) comparer context.

```cpp
class ComparerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ComparerContext](./comparercontext/)() |  |
| [get_AcceptRevisions](./get_acceptrevisions/)() const | Indica se accettare le revisioni nei documenti prima di confrontarli. Se i documenti confrontati contengono revisioni e questo flag è impostato su false, il processore rifiuterà le revisioni. Il valore predefinito è **true**. |
| [get_Author](./get_author/)() const | L'autore da assegnare alle revisioni create durante il confronto dei documenti. |
| [get_CompareOptions](./get_compareoptions/)() const | Opzioni utilizzate durante il confronto dei documenti. |
| [get_DateTime](./get_datetime/)() const | La data e l'ora assegnate alle revisioni create durante il confronto dei documenti. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Impostazioni [Font](../../aspose.words/font/) utilizzate dal processore. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Opzioni di layout [Document](../../aspose.words/document/) utilizzate dal processore. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Callback di avviso utilizzato dal processore. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_AcceptRevisions](./set_acceptrevisions/)(bool) | Indica se accettare le revisioni nei documenti prima di confrontarli. Se i documenti confrontati contengono revisioni e questo flag è impostato su false, il processore rifiuterà le revisioni. Il valore predefinito è **true**. |
| [set_Author](./set_author/)(const System::String\&) | L'autore da assegnare alle revisioni create durante il confronto dei documenti. |
| [set_DateTime](./set_datetime/)(System::DateTime) | La data e l'ora assegnate alle revisioni create durante il confronto dei documenti. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Impostazioni [Font](../../aspose.words/font/) utilizzate dal processore. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Callback di avviso utilizzato dal processore. |
| static [Type](./type/)() |  |
## Vedi anche

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
