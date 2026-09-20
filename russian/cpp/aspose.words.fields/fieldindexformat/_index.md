---
title: "Aspose::Words::Fields::FieldIndexFormat перечисление"
linktitle: "FieldIndexFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldIndexFormat перечисление. Указывает форматирование полей FieldIndex в документе на C++."
type: docs
weight: 129000
url: /ru/cpp/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enum


Указывает форматирование полей [FieldIndex](../fieldindex/) в документе.

```cpp
enum class FieldIndexFormat
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Шаблон | 0 | Из шаблона. |
| Классический | 1 | Классический. |
| Элегантный | 2 | Элегантный. |
| Modern | 3 | Современный. |
| Маркированный | 4 | Маркированный. |
| Формальный | 5 | Формальный. |
| Простой | 6 | Простой. |


## Примеры



Показывает, как форматировать поля [FieldIndex](../fieldindex/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"A");
builder->InsertBreak(Aspose::Words::BreakType::LineBreak);
builder->InsertField(u"XE \"A\"");
builder->Write(u"B");

builder->InsertField(u" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", nullptr);

doc->get_FieldOptions()->set_FieldIndexFormat(Aspose::Words::Fields::FieldIndexFormat::Fancy);
doc->UpdateFields();

doc->Save(get_ArtifactsDir() + u"Field.SetFieldIndexFormat.docx");
```

## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
