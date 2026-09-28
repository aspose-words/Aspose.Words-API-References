---
title: "Aspose::Words::PageSetup::get_LineNumberCountBy метод"
linktitle: "get_LineNumberCountBy"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_LineNumberCountBy метод. Возвращает или задает числовой шаг для номеров строк в C++."
type: docs
weight: 23000
url: /ru/cpp/aspose.words/pagesetup/get_linenumbercountby/
---
## PageSetup::get_LineNumberCountBy method


Возвращает или задает числовой шаг для номеров строк.

```cpp
int32_t Aspose::Words::PageSetup::get_LineNumberCountBy()
```


## Примеры



Показано, как включить нумерацию строк для раздела.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Мы можем использовать объект PageSetup раздела, чтобы отображать номера слева от строк текста раздела.
// Это такое же поведение, как у объекта List,
// но охватывает весь раздел и не изменяет текст никаким образом.
// Наш раздел будет перезапускать нумерацию на каждой новой странице с 1 и отображать номер,
// если он кратен 3, на 50pt слева от строки.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_LineStartingNumber(1);
pageSetup->set_LineNumberCountBy(3);
pageSetup->set_LineNumberRestartMode(Aspose::Words::LineNumberRestartMode::RestartPage);
pageSetup->set_LineNumberDistanceFromText(50.0);

for (int32_t i = 1; i <= 25; i++)
{
    builder->Writeln(System::String::Format(u"Line {0}.", i));
}

// Счётчик строк будет пропускать любой абзац с флагом "SuppressLineNumbers", установленным в "true".
// Этот абзац находится на 15‑й строке, которая кратна 3, и поэтому обычно отображал бы номер строки.
// Счётчик строк раздела также будет игнорировать эту строку, считать следующую строкой 15‑й,
// и продолжит подсчёт с этой точки дальше.
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(14)->get_ParagraphFormat()->set_SuppressLineNumbers(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.LineNumbers.docx");
```

## См. также

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
