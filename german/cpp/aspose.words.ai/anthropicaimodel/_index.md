---
title: "Aspose::Words::AI::AnthropicAiModel class"
linktitle: "AnthropicAiModel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::AnthropicAiModel class. Eine abstrakte Klasse, die die Integration mit den KI-Modellen von Anthropic innerhalb von Aspose.Words in C++ darstellt."
type: docs
weight: 1250
url: /de/cpp/aspose.words.ai/anthropicaimodel/
---
## AnthropicAiModel class


Eine abstrakte Klasse, die die Integration mit den [AI](../)-Modellen von Anthropic innerhalb von [Aspose.Words](../../aspose.words/) darstellt.

```cpp
class AnthropicAiModel : public Aspose::Words::AI::AiModel
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [AnthropicAiModel](./anthropicaimodel/)() |  |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Überprüft die Grammatik des bereitgestellten Dokuments. Dieser Vorgang nutzt das verbundene [AI](../)-Modell zur Grammatikprüfung des Dokuments. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Erstellt eine neue Instanz der Klasse [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Liest oder setzt die Anzahl der Millisekunden, die gewartet werden, bevor die Anfrage an das [AI](../)-Modell abläuft. Der Standardwert beträgt 100.000 Millisekunden (100 Sekunden). |
| [get_Url](./get_url/)() override | Liest die URL des Modells. Der Standardwert ist "https://api.anthropic.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Setter für [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Setzt die URL des Modells. Der Standardwert ist "https://api.anthropic.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Erstellt eine Zusammenfassung des angegebenen Dokuments, mit Optionen zur Anpassung der Länge der Zusammenfassung. Dieser Vorgang nutzt das verbundene [AI](../)-Modell zur Inhaltsverarbeitung. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Erstellt Zusammenfassungen für ein Array von Dokumenten, mit Optionen zur Steuerung der Zusammenfassungslänge und anderer Einstellungen. Diese Methode nutzt das verbundene [AI](../)-Modell zur Verarbeitung jedes Dokuments im Array. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Übersetzt das bereitgestellte Dokument in die angegebene Zielsprache. Dieser Vorgang nutzt das verbundene [AI](../)-Modell zur Inhaltsübersetzung. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Setzt einen angegebenen API-Schlüssel für das Modell. |
## Siehe auch

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
