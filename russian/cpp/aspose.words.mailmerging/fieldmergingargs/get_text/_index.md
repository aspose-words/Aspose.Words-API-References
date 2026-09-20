---
title: "Метод Aspose::Words::MailMerging::FieldMergingArgs::get_Text"
linktitle: "get_Text"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::MailMerging::FieldMergingArgs::get_Text. Получает или задает текст, который будет вставлен в документ для текущего поля слияния в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.mailmerging/fieldmergingargs/get_text/
---
## FieldMergingArgs::get_Text method


Получает или задает текст, который будет вставлен в документ для текущего поля слияния.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgs::get_Text() const
```

## Примечания


Когда вызывается ваш обработчик событий, это свойство устанавливается в **null**.

Если оставить Text как **null**, движок слияния почты вставит [FieldValue](../../fieldmergingargsbase/get_fieldvalue/) вместо поля слияния.

Если вы задаете Text любой строкой (включая пустую), строка будет вставлена в документ вместо поля слияния.
## См. также

* Class [FieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
