---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements metod"
linktitle: "get_IgnoreNoscriptElements"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements metod. Hämtar eller anger ett värde som indikerar om <noscript>-HTML-element ska ignoreras. Standardvärdet är false i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.loading/htmlloadoptions/get_ignorenoscriptelements/
---
## HtmlLoadOptions::get_IgnoreNoscriptElements method


Hämtar eller anger ett värde som indikerar om <noscript>-HTML-element ska ignoreras. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements() const
```


## Exempel



Visar hur man ignorerar <noscript>-HTML-element.
```cpp
const System::String html = u"\r\n                <html>\r\n                  <head>\r\n                    <title>NOSCRIPT</title>\r\n                      <meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n                      <script type=\"text/javascript\">\r\n                        alert(\"Hello, world!\");\r\n                      </script>\r\n                  </head>\r\n                <body>\r\n                  <noscript><p>Your browser does not support JavaScript!</p></noscript>\r\n                </body>\r\n                </html>";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_IgnoreNoscriptElements(ignoreNoscriptElements);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.IgnoreNoscriptElements.pdf");
```

## Se även

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
