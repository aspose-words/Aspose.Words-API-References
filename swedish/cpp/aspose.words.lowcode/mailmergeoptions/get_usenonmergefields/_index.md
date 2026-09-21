---
title: "Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields‑metod"
linktitle: "get_UseNonMergeFields"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields‑metod. När true, anger att förutom MERGEFIELD‑fält utförs mail‑merge även i vissa andra fälttyper och i \"{{fieldName}}\"‑taggar i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.lowcode/mailmergeoptions/get_usenonmergefields/
---
## MailMergeOptions::get_UseNonMergeFields method


När **true**, specificerar att förutom MERGEFIELD-fält utförs sammanslagning i vissa andra fälttyper och även i \"{{fieldName}}\"-taggar.

```cpp
bool Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields() const
```

## Anmärkningar


Normalt utförs mail‑merge endast i MERGEFIELD‑fält, men flera kunder hade sina rapporter byggda med andra fält och hade många dokument skapade på detta sätt. För att förenkla migrering (och eftersom detta tillvägagångssätt användes av flera kunder) infördes möjligheten att utföra mail‑merge i andra fält.

När [UseNonMergeFields](./) är inställd på **true**, kommer Aspose.Words att utföra mail‑merge i följande fält:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Dessutom, när [UseNonMergeFields](./) är inställd på **true**, Aspose.Words kommer att utföra postfogningssammanfogning i texttaggar "{{fieldName}}". Dessa är inte fält, utan bara texttaggar.
## Se även

* Class [MailMergeOptions](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
