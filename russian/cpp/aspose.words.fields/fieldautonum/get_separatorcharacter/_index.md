---
title: "Метод Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter"
linktitle: "get_SeparatorCharacter"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter method. Получает или задает символ разделителя, используемый в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldautonum/get_separatorcharacter/
---
## FieldAutoNum::get_SeparatorCharacter method


Получает или задаёт символ-разделитель, который будет использоваться.

```cpp
System::String Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter()
```


## Примеры



Показывает, как нумеровать абзацы с помощью полей autonum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Каждое поле AUTONUM отображает текущее значение текущего счёта полей AUTONUM,
// позволяя нам автоматически нумеровать элементы, как в нумерованном списке.
// Это поле будет отображать число "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 1.");

ASSERT_EQ(u" AUTONUM ", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 2.");

// Символ-разделитель, который появляется в результате поля сразу после числа, по умолчанию является точкой.
// Если оставить это свойство null, наше второе поле AUTONUM отобразит "2." в документе.
ASSERT_TRUE(System::TestTools::IsNull(field->get_SeparatorCharacter()));

// Мы можем установить это свойство, чтобы использовать первый символ его строки в качестве нового символа-разделителя.
// В этом случае наше поле AUTONUM теперь будет отображать "2:".
field->set_SeparatorCharacter(u":");

ASSERT_EQ(u" AUTONUM  \\s :", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.AUTONUM.docx");
```

## См. также

* Class [FieldAutoNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
