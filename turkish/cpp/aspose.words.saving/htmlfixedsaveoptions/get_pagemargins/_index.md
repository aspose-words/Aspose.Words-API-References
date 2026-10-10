---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins metodu"
linktitle: "get_PageMargins"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins metodu. HTML belgesindeki sayfalar etrafındaki kenar boşluklarını belirtir. Kenar boşlukları değeri puan cinsinden ölçülür ve 0'a eşit veya daha büyük olmalıdır. Varsayılan değer C++'da 10 puandır."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagemargins/
---
## HtmlFixedSaveOptions::get_PageMargins method


HTML belgesindeki sayfaların etrafındaki kenar boşluklarını belirtir. Kenar boşluğu değeri puan cinsinden ölçülür ve 0'a eşit ya da daha büyük olmalıdır. Varsayılan değer 10 puandır.

```cpp
double Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins() const
```

## Açıklamalar


Değerine bağlıdır [PageHorizontalAlignment](../get_pagehorizontalalignment/) özelliği:

* Defines top, bottom and left page margins if the value is [Left](../../htmlfixedpagehorizontalalignment/).
* Defines top, bottom and right page margins if the value is [Right](../../htmlfixedpagehorizontalalignment/).
* Defines top and bottom page margins if the value is [Center](../../htmlfixedpagehorizontalalignment/).



## Örnekler



Bir belgeyi HTML olarak kaydederken sayfa kenar boşluklarını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_PageMargins(15);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins/styles.css");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }")->get_Success());
```

## Ayrıca Bakınız

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
