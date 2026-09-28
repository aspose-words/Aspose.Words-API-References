---
title: "Метод Aspose::Words::Fields::FieldAdvance::get_DownOffset"
linktitle: "get_DownOffset"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldAdvance::get_DownOffset. Получает или задает количество пунктов, на которое текст, следующий за полем, должен быть смещён вниз в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldadvance/get_downoffset/
---
## FieldAdvance::get_DownOffset method


Получает или задаёт количество пунктов, на которое текст, следующий за полем, должен быть смещён вниз.

```cpp
System::String Aspose::Words::Fields::FieldAdvance::get_DownOffset()
```


## Примеры



Показывает, как вставить поле ADVANCE и изменить его свойства.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// Ниже представлены два способа использования поля ADVANCE для корректировки позиции следующего за ним текста.
// Эффекты поля ADVANCE продолжают применяться до конца абзаца,
// или другое поле ADVANCE обновляет значения смещения/координат.
// 1 - Указать направленное смещение:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 - Переместить текст в позицию, заданную координатами:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## См. также

* Class [FieldAdvance](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
