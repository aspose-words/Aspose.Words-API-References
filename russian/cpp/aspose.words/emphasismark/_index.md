---
title: "Aspose::Words::EmphasisMark enum"
linktitle: "EmphasisMark"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::EmphasisMark enum. Указывает возможные типы знаков выделения в C++."
type: docs
weight: 89000
url: /ru/cpp/aspose.words/emphasismark/
---
## EmphasisMark enum


Указывает возможные типы знака ударения.

```cpp
enum class EmphasisMark
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Нет знака выделения. |
| OverSolidCircle | 1 | Знак выделения — сплошной черный круг, отображаемый над текстом. |
| OverComma | 2 | Знак выделения — символ запятой, отображаемый над текстом. |
| OverWhiteCircle | 3 | Знак выделения — пустой белый круг, отображаемый над текстом. |
| UnderSolidCircle | 4 | Знак выделения — сплошной черный круг, отображаемый под текстом. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
