---
title: "Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName метод"
linktitle: "get_DocumentFieldName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName метод. Возвращает имя поля слияния, указанное в документе, в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.mailmerging/fieldmergingargsbase/get_documentfieldname/
---
## FieldMergingArgsBase::get_DocumentFieldName method


Получает имя поля слияния, как указано в документе.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName() const
```

## Примечания


Если у вас есть сопоставление имени поля документа с другим именем поля источника данных, то это оригинальное имя поля, указанное в документе.

Если вы указали префикс имени поля, например "Image:MyFieldName" в документе, то [DocumentFieldName](./) возвращает имя поля без префикса, то есть "MyFieldName".
## См. также

* Class [FieldMergingArgsBase](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
