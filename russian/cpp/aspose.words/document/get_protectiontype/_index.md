---
title: "Aspose::Words::Document::get_ProtectionType метод"
linktitle: "get_ProtectionType"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_ProtectionType. Получает текущий активный тип защиты документа в C++."
type: docs
weight: 44000
url: /ru/cpp/aspose.words/document/get_protectiontype/
---
## Document::get_ProtectionType method


Получает текущий активный тип защиты документа.

```cpp
Aspose::Words::ProtectionType Aspose::Words::Document::get_ProtectionType()
```

## Примечания


Это свойство позволяет получить текущий установленный тип защиты документа. Чтобы изменить тип защиты документа, используйте методы [Protect()](../) и [Unprotect](../unprotect/).

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
