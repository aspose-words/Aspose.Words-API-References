---
title: "Aspose::Words::Fields::FieldListNum::get_ListLevel method"
linktitle: "get_ListLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldListNum::get_ListLevel method. Получает или задает уровень в списке, переопределяя поведение поля по умолчанию в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fields/fieldlistnum/get_listlevel/
---
## FieldListNum::get_ListLevel method


Получает или задает уровень в списке, переопределяя поведение поля по умолчанию.

```cpp
System::String Aspose::Words::Fields::FieldListNum::get_ListLevel()
```


## Примеры



Показывает, как нумеровать абзацы с помощью полей LISTNUM.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Поля LISTNUM отображают число, которое увеличивается в каждом поле LISTNUM.
// Эти поля также имеют разнообразные параметры, позволяющие использовать их для имитации нумерованных списков.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// Списки по умолчанию начинают счёт с 1, но мы можем задать другое значение, например 0.
// Это поле отобразит "0)".
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// Поля LISTNUM поддерживают отдельные счётчики для каждого уровня списка.
// Вставка поля LISTNUM в тот же абзац, что и другое поле LISTNUM
// увеличивает уровень списка вместо счёта.
// Следующее поле продолжит счёт, который мы начали выше, и отобразит значение "1" на уровне списка 1.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Это поле начнёт счёт на уровне списка 2. Оно отобразит значение "1".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Это поле начнёт счёт на уровне списка 3. Оно отобразит значение "1".
// Разные уровни списка имеют разное форматирование,
// поэтому эти поля вместе отобразят значение "1)a)i)".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// Следующее поле LISTNUM, которое мы вставим, продолжит счёт на уровне списка
// на котором находилось предыдущее поле LISTNUM.
// Мы можем использовать свойство "ListLevel", чтобы перейти к другому уровню списка.
// Если бы это поле LISTNUM осталось на уровне списка 3, оно отобразило бы "ii)",
// но, поскольку мы переместили его на уровень списка 2, оно продолжает счёт на этом уровне и отображает "b)".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// Мы можем задать свойство ListName, чтобы поле имитировало другой тип поля AUTONUM.
// "NumberDefault" имитирует AUTONUM, "OutlineDefault" имитирует AUTONUMOUT,
// а "LegalDefault" имитирует поля AUTONUMLGL.
// Имя списка "OutlineDefault" с 1 в качестве начального номера приведет к отображению "I.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// Имя списка ListName не переносится из предыдущего поля, поэтому нам потребуется установить его для каждого нового поля.
// Это поле продолжает счет с другим именем списка и отображает "II.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## См. также

* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
