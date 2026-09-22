---
title: "Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields metodu"
linktitle: "get_UseNonMergeFields"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields metodu. true olduğunda, MERGEFIELD alanlarına ek olarak, posta birleştirmenin başka bazı alan türlerine ve ayrıca \"{{fieldName}}\" etiketlerine de C++ içinde uygulanacağını belirtir."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.lowcode/mailmergeoptions/get_usenonmergefields/
---
## MailMergeOptions::get_UseNonMergeFields method


**true** olduğunda, MERGEFIELD alanlarına ek olarak posta birleştirmenin bazı diğer alan türlerine ve ayrıca "{{fieldName}}" etiketlerine de uygulandığını belirtir.

```cpp
bool Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields() const
```

## Açıklamalar


Normalde, posta birleştirme yalnızca MERGEFIELD alanlarına uygulanır, ancak birkaç müşteri raporlamasını başka alanları kullanarak oluşturmuş ve bu şekilde birçok belge üretmiştir. Geçişi basitleştirmek (ve bu yaklaşımın birkaç müşteri tarafından bağımsız olarak kullanılması nedeniyle) diğer alanlara posta birleştirme yeteneği eklenmiştir.

[UseNonMergeFields](./) **true** olarak ayarlandığında, Aspose.Words aşağıdaki alanlara posta birleştirme yapacaktır:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Ayrıca, [UseNonMergeFields](./) **true** olarak ayarlandığında, Aspose.Words "{{fieldName}}" metin etiketlerine posta birleştirme yapacaktır. Bunlar alan değildir, sadece metin etiketleridir.
## Ayrıca Bakınız

* Class [MailMergeOptions](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
