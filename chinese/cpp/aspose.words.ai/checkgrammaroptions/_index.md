---
title: "Aspose::Words::AI::CheckGrammarOptions 类"
linktitle: "CheckGrammarOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::CheckGrammarOptions 类。允许在使用 C++ 的 AI 检查文档语法时指定各种选项。"
type: docs
weight: 1500
url: /zh/cpp/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class


允许在使用 [AI](../) 检查文档语法时指定各种选项。

```cpp
class CheckGrammarOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [CheckGrammarOptions](./checkgrammaroptions/)() |  |
| [get_ImproveStylistics](./get_improvestylistics/)() const | 允许指定 [AI](../) 是否尝试改进被校对文本的文体。默认值为 **false**。 |
| [get_MakeRevisions](./get_makerevisions/)() const | 允许指定返回的校对文本是最终文档还是修订文档。默认值为 **false**。 |
| [get_PreserveFormatting](./get_preserveformatting/)() const | 允许指定 [CheckGrammar()](../aimodel/checkgrammar/) 是否尝试保留原始文档的布局和格式。默认值为 **true**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImproveStylistics](./set_improvestylistics/)(bool) | 允许指定 [AI](../) 是否尝试改进被校对文本的文体。默认值为 **false**。 |
| [set_MakeRevisions](./set_makerevisions/)(bool) | 允许指定返回的校对文本是最终文档还是修订文档。默认值为 **false**。 |
| [set_PreserveFormatting](./set_preserveformatting/)(bool) | 允许指定 [CheckGrammar()](../aimodel/checkgrammar/) 是否尝试保留原始文档的布局和格式。默认值为 **true**。 |
| static [Type](./type/)() |  |

## 示例



展示如何检查文档的语法。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// 使用 OpenAI 生成式语言模型。
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## 另见

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
