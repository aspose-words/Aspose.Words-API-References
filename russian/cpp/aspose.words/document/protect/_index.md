---
title: "Aspose::Words::Document::Protect метод"
linktitle: "Protect"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::Protect метод. Защищает документ от изменений без изменения существующего пароля или назначает случайный пароль в C++."
type: docs
weight: 67000
url: /ru/cpp/aspose.words/document/protect/
---
## Document::Protect(Aspose::Words::ProtectionType) method


Защищает документ от изменений без изменения существующего пароля или назначает случайный пароль.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| тип | Aspose::Words::ProtectionType | Указывает тип защиты документа. |
## Примечания


Когда документ защищён, пользователь может вносить только ограниченные изменения, такие как добавление аннотаций, создание правок или заполнение формы.

Когда вы защищаете документ, и у документа уже установлен пароль защиты, существующий пароль не изменяется.

Когда вы защищаете документ, и у документа нет пароля защиты, этот метод назначает случайный пароль, который делает невозможным снятие защиты в Microsoft Word, но вы всё равно можете снять защиту в Aspose.Words, так как при снятии защиты пароль не требуется.

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

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Protect(Aspose::Words::ProtectionType, const System::String\&) method


Защищает документ от изменений и при желании задаёт пароль защиты.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type, const System::String &password)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| тип | Aspose::Words::ProtectionType | Указывает тип защиты документа. |
| password | const System::String\& | Пароль для защиты документа. Укажите **null** или пустую строку, если хотите защитить документ без пароля. |
## Примечания


Когда документ защищён, пользователь может вносить только ограниченные изменения, такие как добавление аннотаций, создание правок или заполнение формы.

Обратите внимание, что защита документа отличается от защиты от записи. Защита от записи указывается с помощью [WriteProtection](../get_writeprotection/).

## Примеры



Показывает, как защитить и снять защиту с документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"password");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// Если мы откроем этот документ в Microsoft Word с намерением отредактировать его,
// нам потребуется ввести пароль, чтобы пройти защиту.
doc->Save(get_ArtifactsDir() + u"Document.Protect.docx");

// Обратите внимание, что защита применяется только к пользователям Microsoft Word, открывающим наш документ.
// Мы не шифровали документ никаким образом, и нам не нужен пароль для программного открытия и редактирования его.
auto protectedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.Protect.docx");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, protectedDoc->get_ProtectionType());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(protectedDoc);
builder->Writeln(u"Text added to a protected document.");

// Существует два способа снять защиту с документа.
// 1 - Без пароля:
doc->Unprotect();

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());

doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

doc->Unprotect(u"WrongPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// 2 - С правильным паролем:
doc->Unprotect(u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());
```

## См. также

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
