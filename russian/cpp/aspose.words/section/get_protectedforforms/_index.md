---
title: "Aspose::Words::Section::get_ProtectedForForms метод"
linktitle: "get_ProtectedForForms"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Section::get_ProtectedForForms метод. True, если раздел защищён для форм. Когда раздел защищён для форм, пользователи могут выбирать и изменять текст только в полях формы в Microsoft Word в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words/section/get_protectedforforms/
---
## Section::get_ProtectedForForms method


Истина, если раздел защищён для форм. Когда раздел защищён для форм, пользователи могут выделять и изменять текст только в полях формы в Microsoft Word.

```cpp
bool Aspose::Words::Section::get_ProtectedForForms()
```


## Примеры



Показывает, как отключить защиту для раздела.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Применить защиту от записи ко всем разделам в документе.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// Отключить защиту от записи для первого раздела.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// В этом выходном документе мы сможем свободно редактировать первый раздел,
// и мы сможем редактировать только содержимое поля формы во втором разделе.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## См. также

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
