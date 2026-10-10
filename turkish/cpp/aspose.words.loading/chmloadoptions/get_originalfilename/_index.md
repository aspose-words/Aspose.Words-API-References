---
title: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName yöntemi"
linktitle: "get_OriginalFileName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName yöntemi. CHM dosyasının adını verir. Varsayılan değer C++'ta null'dur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.loading/chmloadoptions/get_originalfilename/
---
## ChmLoadOptions::get_OriginalFileName method


CHM dosyasının adı. Varsayılan değer **null**'dır.

```cpp
System::String Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName() const
```

## Açıklamalar


CHM belgeleri, aynı belgeye dosya adıyla referans veren bağlantılar içerebilir. Aspose.Words bu tür bağlantıları destekler ve genellikle bir bağlantı tarafından referans edilen dosyanın yüklenen dosya olup olmadığını kontrol etmek için [OriginalFileName](../../../aspose.words/document/get_originalfilename/) kullanır. Bir belge bir akıştan yüklendiğinde, orijinal dosya adı bu özellik aracılığıyla açıkça belirtilmelidir, çünkü otomatik olarak belirlenemez.

Bir CHM belgesi bir dosyadan yüklendiğinde ve bu özellik için null olmayan bir değer belirtilirse, değer [OriginalFileName](../../../aspose.words/document/get_originalfilename/) içinde depolanan dosyanın gerçek adının üzerine öncelik kazanır.

## Örnekler



"ms-its:myfile.chm::/index.htm" gibi URL'lerin nasıl çözüleceğini gösterir.
```cpp
// Belgemiz "ms-its:amhelp.chm::....htm" gibi URL'ler içeriyor, ancak farklı bir adı var,
// Bu nedenle dosya bağlantıları HTML olarak kaydedildikten sonra çalışmaz.
// Bu davranışı önlemek için 'ChmLoadOptions' içinde özgün dosya adını tanımlamamız gerekiyor.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## Ayrıca Bakınız

* Class [ChmLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
