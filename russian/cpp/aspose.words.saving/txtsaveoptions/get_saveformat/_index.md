---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat method"
linktitle: "get_SaveFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat метод. Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. В C++ может быть только Text."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.saving/txtsaveoptions/get_saveformat/
---
## TxtSaveOptions::get_SaveFormat method


Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть только [Text](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
