---
title: "Aspose::Words::DocumentBuilder::get_Italic метод"
linktitle: "get_Italic"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::get_Italic метод. True, если шрифт отформатирован как курсив в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words/documentbuilder/get_italic/
---
## DocumentBuilder::get_Italic method


True, если шрифт оформлен курсивом.

```cpp
bool Aspose::Words::DocumentBuilder::get_Italic()
```


## Примеры



Показывает, как заполнять MERGEFIELDы данными с помощью DocumentBuilder вместо слияния почты.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте несколько MERGEFIELDов, которые принимают данные из столбцов с тем же именем в источнике данных во время слияния почты,
// а затем заполните их вручную.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
