---
title: "Aspose::Words::Properties::DocumentSecurity перечисление"
linktitle: "DocumentSecurity"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::DocumentSecurity перечисление. Используется как значение свойства Security. Указывает уровень безопасности документа как числовое значение в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enum


Используется как значение свойства [Security](../builtindocumentproperties/get_security/). Указывает уровень безопасности документа как числовое значение.

```cpp
enum class DocumentSecurity
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Для свойства не указаны состояния безопасности. |
| PasswordProtected | 1 | Документ защищён паролем. (Примечание: до сих пор такой случай не встречался в документах). |
| ReadOnlyRecommended | 2 | Документ должен быть открыт только для чтения, если это возможно, но настройку можно переопределить. |
| ReadOnlyEnforced | 4 | Документ всегда должен открываться только для чтения. |
| ReadOnlyExceptAnnotations | 8 | Документ всегда должен открываться только для чтения, за исключением аннотаций. |


## Примеры



Показывает, как использовать свойства документа для отображения уровня безопасности документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::None, doc->get_BuiltInDocumentProperties()->get_Security());

// Если мы настроим документ как только для чтения, он будет отображать этот статус с помощью встроенного свойства "Security".
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyRecommended, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx")->get_BuiltInDocumentProperties()->get_Security());

// Защитите документ от записи, а затем проверьте его уровень безопасности.
doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->get_WriteProtection()->SetPassword(u"MyPassword");

ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));
ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyEnforced, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx")->get_BuiltInDocumentProperties()->get_Security());

// "Security" — описательное свойство. Мы можем изменить его значение вручную.
doc = System::MakeObject<Aspose::Words::Document>();

doc->Protect(Aspose::Words::ProtectionType::AllowOnlyComments, u"MyPassword");
doc->get_BuiltInDocumentProperties()->set_Security(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx")->get_BuiltInDocumentProperties()->get_Security());
```

## См. также

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
