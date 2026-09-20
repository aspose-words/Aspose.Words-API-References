---
title: "Перечисление Aspose::Words::ProtectionType"
linktitle: "ProtectionType"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::ProtectionType. Тип защиты для документа на C++."
type: docs
weight: 111000
url: /ru/cpp/aspose.words/protectiontype/
---
## ProtectionType enum


Тип защиты документа.

```cpp
enum class ProtectionType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| AllowOnlyComments | 1 | Пользователь может только изменять комментарии в документе. |
| AllowOnlyFormFields | 2 | Пользователь может только вводить данные в поля формы в документе. |
| AllowOnlyRevisions | 0 | Пользователь может только добавлять метки ревизий в документ. |
| ReadOnly | 3 | Изменения в документе не допускаются. Доступно, начиная с Microsoft Word 2003. |
| NoProtection | -1 | Документ не защищён. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
