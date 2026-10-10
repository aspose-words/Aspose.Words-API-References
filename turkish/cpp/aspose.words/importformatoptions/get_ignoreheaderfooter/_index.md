---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter method"
linktitle: "get_IgnoreHeaderFooter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter yöntemi. KeepSourceFormatting modu kullanıldığında başlık/altbilgi içeriğinin kaynak biçimlendirmesinin göz ardı edilip edilmediğini belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'da true'dur."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/importformatoptions/get_ignoreheaderfooter/
---
## ImportFormatOptions::get_IgnoreHeaderFooter method


Başlık/altbilgi içeriğinin kaynak biçimlendirmesinin göz ardı edilip edilmediğini belirten bir boolean değer alır veya ayarlar, eğer [KeepSourceFormatting](../../importformatmode/) modu kullanılıyorsa. Varsayılan değer **true**'dır.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter() const
```


## Örnekler



Başlık/altbilgi içeriğinin kaynak biçimlendirmesinin göz ardı edilip edilmediğini nasıl belirteceğinizi gösterir.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// 'IgnoreHeaderFooter' false ise, başlık/altbilgi içeriği için orijinal biçimlendirme
// \"Header and footer types.docx\" dosyasından kullanılacak.
// Eğer 'IgnoreHeaderFooter' true ise, başlık/altbilgi içeriği için biçimlendirme
// \"Document.docx\" dosyasından kullanılacak.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreHeaderFooter(false);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

## Ayrıca Bakınız

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
