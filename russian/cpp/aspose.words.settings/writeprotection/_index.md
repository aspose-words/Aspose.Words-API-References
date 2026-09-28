---
title: "Класс Aspose::Words::Settings::WriteProtection"
linktitle: "WriteProtection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Settings::WriteProtection. Указывает параметры защиты записи для документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.settings/writeprotection/
---
## WriteProtection class


Указывает настройки защиты от записи для документа. Чтобы узнать больше, посетите статью документации [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class WriteProtection : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_IsWriteProtected](./get_iswriteprotected/)() | Возвращает **true**, когда установлен пароль защиты записи. |
| [get_ReadOnlyRecommended](./get_readonlyrecommended/)() const | Указывает, рекомендовал ли автор документа открыть его в режиме только для чтения. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ReadOnlyRecommended](./set_readonlyrecommended/)(bool) | Сеттер для [Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended](./get_readonlyrecommended/). |
| [SetPassword](./setpassword/)(const System::String\&) | Устанавливает пароль защиты записи для документа. |
| static [Type](./type/)() |  |
| [ValidatePassword](./validatepassword/)(const System::String\&) | Возвращает **true**, если указанный пароль совпадает с паролем защиты записи, которым документ был защищён. Если документ не защищён паролем записи, возвращает **false**. |
## Примечания


Защита записи указывает, рекомендовал ли автор открывать документ только для чтения и/или требовать пароль для его изменения.

Защита от записи отличается от защиты документа. Защита от записи указывается в Microsoft Word в параметрах диалогового окна «Сохранить как».

Вы не создаёте экземпляры этого класса напрямую. Вы получаете доступ к настройкам защиты документа через свойство [WriteProtection](../../aspose.words/document/get_writeprotection/).

## Примеры



Показывает, как защитить документ паролем.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// Введите пароль длиной до 15 символов, а затем проверьте статус защиты документа.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// Защита не препятствует программному редактированию документа и не шифрует его содержимое.
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
