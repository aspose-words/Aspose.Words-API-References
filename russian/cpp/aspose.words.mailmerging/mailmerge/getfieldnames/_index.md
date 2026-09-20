---
title: "Aspose::Words::MailMerging::MailMerge::GetFieldNames метод"
linktitle: "GetFieldNames"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::MailMerging::MailMerge::GetFieldNames метод. Возвращает коллекцию имён полей слияния почты, доступных в документе, в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge::GetFieldNames method


Возвращает коллекцию имён полей слияния почты, доступных в документе.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNames()
```

## Примечания


Возвращает полные имена полей слияния, включая необязательный префикс. Не удаляет дублирующие имена полей.

При каждом вызове создаётся новый массив строк.

Включает имена полей "mustache", если [UseNonMergeFields](../get_usenonmergefields/) **true**.
## См. также

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
