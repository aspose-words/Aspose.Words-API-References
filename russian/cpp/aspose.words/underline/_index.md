---
title: "Aspose::Words::Underline enum"
linktitle: "Подчеркивание"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Underline enum. Указывает тип подчеркивания, применяемого к шрифту в C++."
type: docs
weight: 126000
url: /ru/cpp/aspose.words/underline/
---
## Underline enum


Указывает тип подчеркивания, применяемого к шрифту.

```cpp
enum class Underline
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 |  |
| Single | 1 |  |
| Words | 2 |  |
| Double | 3 |  |
| Dotted | 4 |  |
| Thick | 6 |  |
| Dash | 7 |  |
| DashLong | 39 |  |
| DotDash | 9 |  |
| DotDotDash | 10 |  |
| Wavy | 11 |  |
| DottedHeavy | 20 |  |
| DashHeavy | 23 |  |
| DashLongHeavy | 55 |  |
| DotDashHeavy | 25 |  |
| DotDotDashHeavy | 26 |  |
| WavyHeavy | 27 |  |
| WavyDouble | 43 |  |


## Примеры



Показывает, как вставить поле гиперссылки.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Вставьте гиперссылку и выделите её с помощью пользовательского форматирования.
// Гиперссылка будет кликабельным фрагментом текста, который перенаправит нас к месту, указанному в URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + щелчок левой кнопкой мыши по ссылке в тексте в Microsoft Word откроет URL в новом окне веб‑браузера.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
