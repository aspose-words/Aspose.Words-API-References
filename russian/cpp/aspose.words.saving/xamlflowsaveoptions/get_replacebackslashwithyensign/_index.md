---
title: "Метод Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign. Указывает, следует ли заменять символы обратного слеша на знаки йены. Значение по умолчанию — false в C++."
type: docs
weight: 5500
url: /ru/cpp/aspose.words.saving/xamlflowsaveoptions/get_replacebackslashwithyensign/
---
## XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign method


Указывает, должны ли символы обратного слеша заменяться на знаки иены. Значение по умолчанию **false**.

```cpp
bool Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## Примеры



Показывает, как заменять символы обратного слеша на знаки йены (Xaml).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// По умолчанию Aspose.Words имитирует поведение MS Word и не заменяет символы обратного слеша на знаки йены в
// созданные HTML‑документы. Однако предыдущие версии Aspose.Words выполняли такие замены в определённых
// сценариях. Этот флаг обеспечивает обратную совместимость с предыдущими версиями Aspose.Words.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XamlFlowSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

## См. также

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
