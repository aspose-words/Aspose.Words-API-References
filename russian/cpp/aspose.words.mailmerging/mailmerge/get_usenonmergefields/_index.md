---
title: "Метод Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields"
linktitle: "get_UseNonMergeFields"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields. При значении true указывает, что помимо полей MERGEFIELD слияние почты выполняется и в некоторые другие типы полей, а также в теги \"{{fieldName}}\" в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.mailmerging/mailmerge/get_usenonmergefields/
---
## MailMerge::get_UseNonMergeFields method


Когда **true**, указывает, что помимо полей MERGEFIELD слияние почты выполняется и в некоторые другие типы полей, а также в теги "{{fieldName}}".

```cpp
bool Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields() const
```

## Примечания


Обычно слияние почты выполняется только в поля MERGEFIELD, но несколько клиентов построили свою отчетность, используя другие поля, и создали множество документов таким способом. Чтобы упростить миграцию (и потому что этот подход независимо использовался несколькими клиентами), была введена возможность выполнять слияние почты в другие поля.

Когда [UseNonMergeFields](./) установлено в **true**, Aspose.Words будет выполнять слияние почты в следующие поля:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Также, когда [UseNonMergeFields](./) установлено в **true**, Aspose.Words будет выполнять слияние почты в текстовые теги "{{fieldName}}". Это не поля, а просто текстовые теги.
## См. также

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
