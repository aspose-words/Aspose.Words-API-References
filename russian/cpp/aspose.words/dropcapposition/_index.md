---
title: "Aspose::Words::DropCapPosition перечисление"
linktitle: "DropCapPosition"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DropCapPosition перечисление. Указывает положение текста с буквой-капитаном в C++."
type: docs
weight: 87000
url: /ru/cpp/aspose.words/dropcapposition/
---
## DropCapPosition enum


Указывает позицию текста буквицы.

```cpp
enum class DropCapPosition
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | В абзаце нет буквы-капитана. |
| Обычный | 1 | Буква-капитан размещена внутри поля текста в опорном абзаце. |
| Поле | 2 | Буква-капитан размещена за пределами поля текста в опорном абзаце. |


## Примеры



Показывает, как создать букву-капитана.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте один абзац с большой буквой, с которой начинается текст во втором и третьем абзацах.
builder->get_Font()->set_Size(54);
builder->Writeln(u"L");

builder->get_Font()->set_Size(18);
builder->Writeln(System::String(u"orem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder->Writeln(System::String(u"Ut enim ad minim veniam, quis nostrud exercitation ") + u"ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// В настоящее время второй и третий абзацы будут отображаться под первым.
// Мы можем преобразовать первый абзац в букву-капитана для остальных абзацев через его объект \"ParagraphFormat\".
// Установите свойство \"DropCapPosition\" в \"DropCapPosition.Margin\", чтобы разместить букву-капитана
// за пределами левого поля страницы, если наш текст читается слева направо.
// Установите свойство \"DropCapPosition\" в \"DropCapPosition.Normal\", чтобы разместить букву-капитана внутри полей страницы
// и обтекать остальной текст вокруг него.
// \"DropCapPosition.None\" является состоянием по умолчанию для всех абзацев.
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_DropCapPosition(dropCapPosition);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.DropCap.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
