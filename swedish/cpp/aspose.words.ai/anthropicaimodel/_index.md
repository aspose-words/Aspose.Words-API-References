---
title: "Aspose::Words::AI::AnthropicAiModel class"
linktitle: "AnthropicAiModel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::AnthropicAiModel class. En abstrakt klass som representerar integrationen med Anthropic’s AI-modeller inom Aspose.Words i C++."
type: docs
weight: 1250
url: /sv/cpp/aspose.words.ai/anthropicaimodel/
---
## AnthropicAiModel class


En abstrakt klass som representerar integrationen med Anthropic’s [AI](../)-modeller inom [Aspose.Words](../../aspose.words/).

```cpp
class AnthropicAiModel : public Aspose::Words::AI::AiModel
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [AnthropicAiModel](./anthropicaimodel/)() |  |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Kontrollerar grammatiken i det angivna dokumentet. Denna operation utnyttjar den anslutna [AI](../)-modellen för att kontrollera dokumentets grammatik. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Skapar en ny instans av klassen [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Hämtar eller anger antalet millisekunder att vänta innan begäran till [AI](../)-modellen får timeout. Standardvärdet är 100 000 millisekunder (100 sekunder). |
| [get_Url](./get_url/)() override | Hämtar en URL för modellen. Standardvärdet är "https://api.anthropic.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Sättare för [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Anger en URL för modellen. Standardvärdet är "https://api.anthropic.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Genererar en sammanfattning av det angivna dokumentet, med alternativ för att justera sammanfattningens längd. Denna operation utnyttjar den anslutna [AI](../)-modellen för innehållsbehandling. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Genererar sammanfattningar för en matris av dokument, med alternativ för att styra sammanfattningens längd och andra inställningar. Denna metod använder den anslutna [AI](../)-modellen för att bearbeta varje dokument i matrisen. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Översätter det angivna dokumentet till det specificerade målspråket. Denna operation utnyttjar den anslutna [AI](../)-modellen för innehållsöversättning. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Anger en specificerad API-nyckel för modellen. |
## Se även

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
