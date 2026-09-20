---
title: "Метод Aspose::Words::PageSetup::get_Bidi"
linktitle: "get_Bidi"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PageSetup::get_Bidi. Указывает, что этот раздел содержит двунаправленный (сложные сценарии) текст в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/pagesetup/get_bidi/
---
## PageSetup::get_Bidi method


Указывает, что этот раздел содержит двунаправленный (сложные скрипты) текст.

```cpp
bool Aspose::Words::PageSetup::get_Bidi()
```

## Примечания


Когда **true**, столбцы в этом разделе располагаются справа налево.

## Примеры



Показывает, как задать порядок текстовых столбцов в разделе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_TextColumns()->SetCount(3);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 3.");

// Установите свойство "Bidi" в "true", чтобы расположить столбцы, начиная с правой стороны страницы.
// Порядок столбцов будет соответствовать направлению текста справа налево.
// Установите свойство "Bidi" в "false", чтобы расположить столбцы, начиная с левой стороны страницы.
// Порядок столбцов будет соответствовать направлению текста слева направо.
pageSetup->set_Bidi(reverseColumns);

doc->Save(get_ArtifactsDir() + u"PageSetup.Bidi.docx");
```

## См. также

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
