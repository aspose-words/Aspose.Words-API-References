---
title: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions yapıcı"
linktitle: "ChmLoadOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions yapıcı. Bu sınıfın yeni bir örneğini varsayılan değerlerle C++'ta başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions::ChmLoadOptions constructor


Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.

```cpp
Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions()
```


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
