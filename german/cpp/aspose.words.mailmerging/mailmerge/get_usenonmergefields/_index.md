---
title: "Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields method"
linktitle: "get_UseNonMergeFields"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields‑Methode. Wenn true, gibt sie an, dass neben MERGEFIELD‑Feldern der Seriendruck auch in einige andere Feldtypen und in \"{{fieldName}}\"‑Tags in C++ durchgeführt wird."
type: docs
weight: 19000
url: /de/cpp/aspose.words.mailmerging/mailmerge/get_usenonmergefields/
---
## MailMerge::get_UseNonMergeFields method


Wenn **true**, gibt an, dass neben MERGEFIELD‑Feldern der Seriendruck auch in einige andere Feldtypen und in "{{fieldName}}"‑Tags durchgeführt wird.

```cpp
bool Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields() const
```

## Hinweise


Normalerweise wird der Seriendruck nur in MERGEFIELD-Felder durchgeführt, aber mehrere Kunden hatten ihre Berichte mit anderen Feldern erstellt und viele Dokumente auf diese Weise erzeugt. Um die Migration zu vereinfachen (und weil dieser Ansatz von mehreren Kunden unabhängig voneinander verwendet wurde), wurde die Möglichkeit eingeführt, den Seriendruck in andere Felder zu übernehmen.

When [UseNonMergeFields](./) auf **true** gesetzt ist, führt Aspose.Words das Mail-Merge in die folgenden Felder aus:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 \"{FieldName}\" \"\"

Außerdem wird, wenn [UseNonMergeFields](./) auf **true** gesetzt ist, Aspose.Words das Mail-Merge in Text-Tags \"{{fieldName}}\" ausführen. Dies sind keine Felder, sondern nur Text-Tags.
## Siehe auch

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
