---
title: "Aspose::Words::Document::Unprotect метод"
linktitle: "Снять защиту"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::Unprotect метод. Удаляет защиту с документа независимо от пароля в C++."
type: docs
weight: 95000
url: /ru/cpp/aspose.words/document/unprotect/
---
## Document::Unprotect() method


Снимает защиту с документа независимо от пароля.

```cpp
void Aspose::Words::Document::Unprotect()
```

## Примечания


Этот метод снимает защиту с документа, даже если у него установлен пароль защиты.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Unprotect(const System::String\&) method


Снимает защиту с документа, если указан правильный пароль.

```cpp
bool Aspose::Words::Document::Unprotect(const System::String &password)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| password | const System::String\& | Пароль, с помощью которого снимается защита документа. |

### ReturnValue

**true** if a correct password was specified and the document was unprotected.
## Примечания


Этот метод снимает защиту с документа только при указании правильного пароля.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
