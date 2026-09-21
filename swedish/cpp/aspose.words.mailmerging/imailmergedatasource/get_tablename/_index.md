---
title: "Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName metod"
linktitle: "get_TableName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName metod. Returnerar namnet på datakällan i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.mailmerging/imailmergedatasource/get_tablename/
---
## IMailMergeDataSource::get_TableName method


Returnerar namnet på datakällan.

```cpp
virtual System::String Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName()=0
```


### ReturnValue

Namnet på datakällan. Tom sträng om datakällan saknar namn.
## Anmärkningar


Om du implementerar [IMailMergeDataSource](../), returnera namnet på datakällan från denna egenskap.

Aspose.Words använder detta namn för att matcha mot namnet på mail‑sammanfogningsregionen som anges i mall‑dokumentet. Jämförelsen mellan datakällans namn och mail‑sammanfogningsregionens namn är inte skiftlägeskänslig.

## Se även

* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
