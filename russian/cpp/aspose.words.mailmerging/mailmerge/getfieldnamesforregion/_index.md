---
title: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion метод"
linktitle: "GetFieldNamesForRegion"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion метод. Возвращает коллекцию имён полей слияния почты, доступных в регионе, в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## MailMerge::GetFieldNamesForRegion(const System::String\&) method


Возвращает коллекцию имён полей слияния почты, доступных в регионе.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| regionName | const System::String\& | Имя региона (без учёта регистра). |
## Примечания


Возвращает полные имена полей слияния, включая необязательный префикс. Не удаляет дублирующие имена полей.

Если документ содержит несколько регионов с одинаковым именем, обрабатывается первый регион.

При каждом вызове создаётся новый массив строк.

## См. также

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::GetFieldNamesForRegion(const System::String\&, int32_t) method


Возвращает коллекцию имён полей слияния почты, доступных в регионе.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName, int32_t regionIndex)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| regionName | const System::String\& | Имя региона (без учёта регистра). |
| regionIndex | int32_t | Индекс региона (нумерация с нуля). |
## Примечания


Возвращает полные имена полей слияния, включая необязательный префикс. Не удаляет дублирующие имена полей.

Если документ содержит несколько регионов с одинаковым именем, обрабатывается N‑й регион (нумерация с нуля).

При каждом вызове создаётся новый массив строк.

## См. также

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
