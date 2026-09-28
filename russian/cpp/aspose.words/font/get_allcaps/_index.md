---
title: "Aspose::Words::Font::get_AllCaps метод"
linktitle: "get_AllCaps"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_AllCaps. Истина, если шрифт отформатирован заглавными буквами в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/font/get_allcaps/
---
## Font::get_AllCaps method


Истина, если шрифт отформатирован как все заглавные буквы.

```cpp
bool Aspose::Words::Font::get_AllCaps()
```


## Примеры



Показывает, как отформатировать фрагмент, чтобы отображать его содержимое заглавными буквами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Существует два способа заставить фрагмент отображать его текст в верхнем регистре, не меняя содержимое.
// 1 -  Установите флаг AllCaps, чтобы отображать все символы обычными заглавными буквами:
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"all capitals");
run->get_Font()->set_AllCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

// 2 -  Установите флаг SmallCaps, чтобы отображать все символы малыми прописными буквами:
// Если символ в нижнем регистре, он будет отображаться в верхнем регистре
// но будет иметь ту же высоту, что и нижний регистр (x-высоту шрифта).
// Символы, которые изначально были в верхнем регистре, будут выглядеть одинаково.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Small Capitals");
run->get_Font()->set_SmallCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.Caps.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
