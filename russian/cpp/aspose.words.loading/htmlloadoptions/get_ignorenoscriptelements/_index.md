---
title: "Метод Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements"
linktitle: "get_IgnoreNoscriptElements"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements. Получает или задает значение, указывающее, следует ли игнорировать HTML‑элементы <noscript>. Значение по умолчанию — false в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.loading/htmlloadoptions/get_ignorenoscriptelements/
---
## HtmlLoadOptions::get_IgnoreNoscriptElements method


Получает или задает значение, указывающее, следует ли игнорировать элементы HTML <noscript>. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements() const
```


## Примеры



Показывает, как игнорировать HTML‑элементы <noscript>.
```cpp
const System::String html = u"\r\n                <html>\r\n                  <head>\r\n                    <title>NOSCRIPT</title>\r\n                      <meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n                      <script type=\"text/javascript\">\r\n                        alert(\"Hello, world!\");\r\n                      </script>\r\n                  </head>\r\n                <body>\r\n                  <noscript><p>Your browser does not support JavaScript!</p></noscript>\r\n                </body>\r\n                </html>";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_IgnoreNoscriptElements(ignoreNoscriptElements);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.IgnoreNoscriptElements.pdf");
```

## См. также

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
