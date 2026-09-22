---
title: "Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields method"
linktitle: "get_UseNonMergeFields"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields yöntemi. true olduğunda, MERGEFIELD alanlarına ek olarak posta birleştirmenin başka alan türlerine ve ayrıca C++'ta \"{{fieldName}}\" etiketlerine de uygulanacağını belirtir."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.mailmerging/mailmerge/get_usenonmergefields/
---
## MailMerge::get_UseNonMergeFields method


**true** olduğunda, MERGEFIELD alanlarına ek olarak posta birleştirmenin bazı diğer alan türlerine ve ayrıca "{{fieldName}}" etiketlerine de uygulandığını belirtir.

```cpp
bool Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields() const
```

## Açıklamalar


Normalde, posta birleştirme yalnızca MERGEFIELD alanlarına uygulanır, ancak birkaç müşteri raporlamasını başka alanları kullanarak oluşturmuş ve bu şekilde birçok belge üretmiştir. Geçişi basitleştirmek (ve bu yaklaşımın birkaç müşteri tarafından bağımsız olarak kullanılması nedeniyle) diğer alanlara posta birleştirme yeteneği eklenmiştir.

[UseNonMergeFields](./) **true** olarak ayarlandığında, Aspose.Words aşağıdaki alanlara posta birleştirme yapacaktır:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Ayrıca, [UseNonMergeFields](./) **true** olarak ayarlandığında, Aspose.Words "{{fieldName}}" metin etiketlerine posta birleştirme yapacaktır. Bunlar alan değildir, sadece metin etiketleridir.
## Ayrıca Bakınız

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
