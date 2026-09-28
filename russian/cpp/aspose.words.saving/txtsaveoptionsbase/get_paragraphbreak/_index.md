---
title: "Метод Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak"
linktitle: "get_ParagraphBreak"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak. Указывает строку, используемую в качестве разрыва абзаца при экспорте в текстовые форматы в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/txtsaveoptionsbase/get_paragraphbreak/
---
## TxtSaveOptionsBase::get_ParagraphBreak method


Указывает строку, используемую в качестве разрыва абзаца при экспорте в текстовые форматы.

```cpp
System::String Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak() const
```

## Примечания


Значение по умолчанию — [CrLf](../../../aspose.words/controlchar/crlf/).

## Примеры



Показывает, как сохранить .txt документ с пользовательским разрывом абзаца.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Создайте объект "TxtSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ сохранения документа в простой текст.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// Установите "ParagraphBreak" в пользовательское значение, которое мы хотим помещать в конец каждого абзаца.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## См. также

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
