---
title: "Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields метод"
linktitle: "get_UseNonMergeFields"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields метод. Когда true, указывает, что помимо полей MERGEFIELD слияние почты выполняется в некоторые другие типы полей и также в теги \"{{fieldName}}\" в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.lowcode/mailmergeoptions/get_usenonmergefields/
---
## MailMergeOptions::get_UseNonMergeFields method


Когда **true**, указывает, что помимо полей MERGEFIELD слияние почты выполняется и в некоторые другие типы полей, а также в теги "{{fieldName}}".

```cpp
bool Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields() const
```

## Примечания


Обычно слияние почты выполняется только в поля MERGEFIELD, но несколько клиентов построили свою отчетность, используя другие поля, и создали множество документов таким способом. Чтобы упростить миграцию (и потому что этот подход независимо использовался несколькими клиентами), была введена возможность выполнять слияние почты в другие поля.

Когда [UseNonMergeFields](./) установлено в **true**, Aspose.Words будет выполнять слияние почты в следующие поля:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Также, когда [UseNonMergeFields](./) установлено в **true**, Aspose.Words будет выполнять слияние почты в текстовые теги "{{fieldName}}". Это не поля, а просто текстовые теги.
## См. также

* Class [MailMergeOptions](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
