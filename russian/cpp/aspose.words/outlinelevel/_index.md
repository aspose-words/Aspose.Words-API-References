---
title: "Перечисление Aspose::Words::OutlineLevel"
linktitle: "OutlineLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::OutlineLevel. Указывает уровень структуры абзаца в документе на C++."
type: docs
weight: 105000
url: /ru/cpp/aspose.words/outlinelevel/
---
## OutlineLevel enum


Указывает уровень структуры абзаца в документе.

```cpp
enum class OutlineLevel
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Level1 | 0 | Абзац находится на уровне структуры 1 (самый верхний уровень). |
| Level2 | 1 | Параграф находится на уровне структуры 2. |
| Level3 | 2 | Параграф находится на уровне структуры 3. |
| Level4 | 3 | Параграф находится на уровне структуры 4. |
| Level5 | 4 | Параграф находится на уровне структуры 5. |
| Level6 | 5 | Параграф находится на уровне структуры 6. |
| Level7 | 6 | Параграф находится на уровне структуры 7. |
| Level8 | 7 | Параграф находится на уровне структуры 8. |
| Level9 | 8 | Параграф находится на уровне структуры 9. |
| BodyText | 9 | Параграф находится на уровне основного текста. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
