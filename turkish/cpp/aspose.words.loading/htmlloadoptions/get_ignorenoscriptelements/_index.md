---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements metodu"
linktitle: "get_IgnoreNoscriptElements"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements metodu. Alır veya ayarlar <noscript> HTML öğelerini yok sayıp saymayacağını belirten bir değer. Varsayılan değer C++'de false."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.loading/htmlloadoptions/get_ignorenoscriptelements/
---
## HtmlLoadOptions::get_IgnoreNoscriptElements method


İhmal edilip edilmeyeceğini belirten bir değeri alır veya ayarlar <noscript> HTML öğeleri. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements() const
```


## Örnekler



Nasıl <noscript> HTML öğelerinin yok sayılacağını gösterir.
```cpp
const System::String html = u"\r\n                <html>\r\n                  <head>\r\n                    <title>NOSCRIPT</title>\r\n                      <meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n                      <script type=\"text/javascript\">\r\n                        alert(\"Hello, world!\");\r\n                      </script>\r\n                  </head>\r\n                <body>\r\n                  <noscript><p>Your browser does not support JavaScript!</p></noscript>\r\n                </body>\r\n                </html>";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_IgnoreNoscriptElements(ignoreNoscriptElements);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.IgnoreNoscriptElements.pdf");
```

## Ayrıca Bakınız

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
