---
title: "Aspose::Words::ParagraphFormat::get_OutlineLevel метод"
linktitle: "get_OutlineLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_OutlineLevel метод. Указывает уровень структуры (outline) абзаца в документе в C++."
type: docs
weight: 26000
url: /ru/cpp/aspose.words/paragraphformat/get_outlinelevel/
---
## ParagraphFormat::get_OutlineLevel method


Указывает уровень структуры абзаца в документе.

```cpp
Aspose::Words::OutlineLevel Aspose::Words::ParagraphFormat::get_OutlineLevel()
```


## Примеры



Показывает, как настроить уровни структуры параграфов для создания сворачиваемого текста.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Каждый параграф имеет свойство OutlineLevel, которое может принимать любое число от 1 до 9 или значение по умолчанию "BodyText".
// Установка свойства в одно из числовых значений покажет стрелку слева
// в начале параграфа.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level1);
builder->Writeln(u"Paragraph outline level 1.");

// Уровень 1 — самый верхний уровень. Если ниже параграфа более высокого уровня находится параграф с более низким уровнем,
// сворачивание параграфа более высокого уровня свернёт параграф более низкого уровня.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level2);
builder->Writeln(u"Paragraph outline level 2.");

// Два параграфа одного уровня не будут сворачиваться друг с другом,
// и стрелки не сворачивают абзацы, на которые указывают.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level3);
builder->Writeln(u"Paragraph outline level 3.");
builder->Writeln(u"Paragraph outline level 3.");

// Значение по умолчанию "BodyText" является самым низким, которое может сворачивать абзац любого уровня.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::BodyText);
builder->Writeln(u"Paragraph at main text level.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphOutlineLevel.docx");
```

## См. также

* Enum [OutlineLevel](../../outlinelevel/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
