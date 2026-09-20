---
title: "Aspose::Words::Fields::FieldQuote::get_Text метод"
linktitle: "get_Text"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldQuote::get_Text метод. Получает или задает текст для получения в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldquote/get_text/
---
## FieldQuote::get_Text method


Получает или задает текст для получения.

```cpp
System::String Aspose::Words::Fields::FieldQuote::get_Text()
```


## Примеры



Показывает, как использовать поле QUOTE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте поле QUOTE, которое отобразит значение его свойства Text.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Вставьте поле QUOTE и вложите в него поле DATE.
// Поля DATE обновляют своё значение до текущей даты каждый раз, когда мы открываем документ в Microsoft Word.
// Вложение поля DATE в поле QUOTE таким образом заморозит его значение
// на дату, когда мы создали документ.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Обновите все поля, чтобы отобразить их правильные результаты.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```

## См. также

* Class [FieldQuote](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
