---
title: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage метод"
linktitle: "get_AppendDocumentWithNewPage"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage метод. Получает или задает логическое значение, указывающее, следует ли принудительно менять тип первого импортированного раздела на NewPage при вызове AppendDocument(). Значение по умолчанию — true в C++."
type: docs
weight: 3500
url: /ru/cpp/aspose.words/importformatoptions/get_appenddocumentwithnewpage/
---
## ImportFormatOptions::get_AppendDocumentWithNewPage method


Получает или задает логическое значение, указывающее, следует ли принудительно менять тип первого импортированного раздела на [NewPage](../../sectionstart/) при вызове [AppendDocument()](../). Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage() const
```


## Примеры



Показывает, как сохранить исходный тип раздела.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::Continuous);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AppendDocumentWithNewPage(false);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, dstDoc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());
```

## См. также

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
