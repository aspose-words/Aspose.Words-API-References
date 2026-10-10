---
title: "Aspose::Words::AI::AnthropicAiModel sınıfı"
linktitle: "AnthropicAiModel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::AnthropicAiModel sınıfı. C++'ta Aspose.Words içinde Anthropic'in AI modelleriyle entegrasyonu temsil eden soyut bir sınıf."
type: docs
weight: 1250
url: /tr/cpp/aspose.words.ai/anthropicaimodel/
---
## AnthropicAiModel class


Anthropic'in [AI](../) modelleriyle entegrasyonu temsil eden soyut bir sınıf, [Aspose.Words](../../aspose.words/) içinde.

```cpp
class AnthropicAiModel : public Aspose::Words::AI::AiModel
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [AnthropicAiModel](./anthropicaimodel/)() |  |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Sağlanan belgenin dilbilgisini kontrol eder. Bu işlem, belgenin dilbilgisini kontrol etmek için bağlı [AI](../) modelini kullanır. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | [AiModel](../aimodel/) sınıfının yeni bir örneğini oluşturur. |
| [get_Timeout](../aimodel/get_timeout/)() const | [AI](../) modeline yapılan isteğin zaman aşımına uğramadan önce beklenecek milisaniye sayısını alır veya ayarlar. Varsayılan değer 100.000 milisaniyedir (100 saniye). |
| [get_Url](./get_url/)() override | Modelin URL'sini alır. Varsayılan değer "https://api.anthropic.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/) için ayarlayıcı. |
| [set_Url](./set_url/)(System::String) override | Modelin URL'sini ayarlar. Varsayılan değer "https://api.anthropic.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Belirtilen belgenin özetini oluşturur, özetin uzunluğunu ayarlama seçenekleriyle. Bu işlem, içerik işleme için bağlı [AI](../) modelini kullanır. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Belge dizisi için özetler oluşturur, özet uzunluğunu ve diğer ayarları kontrol etme seçenekleriyle. Bu yöntem, dizi içindeki her belgeyi işlemek için bağlı [AI](../) modelini kullanır. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Sağlanan belgeyi belirtilen hedef dile çevirir. Bu işlem, içerik çevirisi için bağlı [AI](../) modelini kullanır. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Model için belirtilen API anahtarını ayarlar. |
## Ayrıca Bakınız

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
