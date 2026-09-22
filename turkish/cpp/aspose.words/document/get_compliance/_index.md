---
title: "Aspose::Words::Document::get_Compliance metodu"
linktitle: "get_Compliance"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_Compliance metodu. Yüklenen belge içeriğinden belirlenen OOXML uyumluluk sürümünü alır. Yalnızca C++'ta OOXML belgeleri için anlamlıdır."
type: docs
weight: 17000
url: /tr/cpp/aspose.words/document/get_compliance/
---
## Document::get_Compliance method


Yüklenen belge içeriğinden belirlenen OOXML uyumluluk sürümünü alır. Yalnızca OOXML belgeleri için anlamlıdır.

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Document::get_Compliance()
```

## Açıklamalar


Yeni bir boş belge oluşturduysanız veya OOXML olmayan bir belge yüklerseniz, [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/) değerini döndürür.

## Örnekler



Yüklenen bir belgenin Open Office XML uyumluluk sürümünü nasıl okuyacağınızı gösterir.
```cpp
// Uyumluluk sürümü, farklı Microsoft Word sürümleriyle oluşturulan belgeler arasında değişir.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.doc");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Ecma376_2006);

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);
```

## Ayrıca Bakınız

* Enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
