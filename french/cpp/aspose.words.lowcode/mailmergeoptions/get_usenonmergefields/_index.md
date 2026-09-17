---
title: "Méthode Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields"
linktitle: "get_UseNonMergeFields"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields. Lorsque true, indique qu’en plus des champs MERGEFIELD, la fusion de courrier est effectuée dans d’autres types de champs et également dans les balises \"{{fieldName}}\" en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.lowcode/mailmergeoptions/get_usenonmergefields/
---
## MailMergeOptions::get_UseNonMergeFields method


Lorsque **true**, spécifie qu'en plus des champs MERGEFIELD, la fusion de courrier est effectuée dans d'autres types de champs et également dans les balises "{{fieldName}}".

```cpp
bool Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields() const
```

## Remarques


Normalement, la fusion de courrier n’est effectuée que dans les champs MERGEFIELD, mais plusieurs clients avaient leurs rapports construits en utilisant d’autres champs et avaient de nombreux documents créés de cette façon. Pour simplifier la migration (et parce que cette approche était utilisée indépendamment par plusieurs clients), la capacité de fusion de courrier dans d’autres champs a été introduite.

Lorsque [UseNonMergeFields](./) est défini sur **true**, Aspose.Words effectuera la fusion de courrier dans les champs suivants :

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

De plus, lorsque [UseNonMergeFields](./) est défini sur **true**, Aspose.Words effectuera la fusion de courrier dans les balises texte "{{fieldName}}". Ce ne sont pas des champs, mais simplement des balises texte.
## Voir aussi

* Class [MailMergeOptions](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
