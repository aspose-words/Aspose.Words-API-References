---
title: "Aspose::Words::Font::get_EmphasisMark метод"
linktitle: "get_EmphasisMark"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Font::get_EmphasisMark метод. Получает или задает знак акцента, применяемый к этому форматированию в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words/font/get_emphasismark/
---
## Font::get_EmphasisMark method


Получает или задаёт знак акцента, применяемый к этому форматированию.

```cpp
Aspose::Words::EmphasisMark Aspose::Words::Font::get_EmphasisMark()
```


## Примеры



Показывает, как добавить дополнительный символ, отображаемый над/под глифом.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Возможные типы знаков выделения:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```

## См. также

* Enum [EmphasisMark](../../emphasismark/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
