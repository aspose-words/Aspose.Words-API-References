---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements método"
linktitle: "get_IgnoreNoscriptElements"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements método. Obtiene o establece un valor que indica si se deben ignorar los elementos HTML <noscript>. El valor predeterminado es false en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.loading/htmlloadoptions/get_ignorenoscriptelements/
---
## HtmlLoadOptions::get_IgnoreNoscriptElements method


Obtiene o establece un valor que indica si se deben ignorar los elementos HTML <noscript>. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements() const
```


## Ejemplos



Muestra cómo ignorar los elementos HTML <noscript>.
```cpp
const System::String html = u"\r\n                <html>\r\n                  <head>\r\n                    <title>NOSCRIPT</title>\r\n                      <meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n                      <script type=\"text/javascript\">\r\n                        alert(\"Hello, world!\");\r\n                      </script>\r\n                  </head>\r\n                <body>\r\n                  <noscript><p>Your browser does not support JavaScript!</p></noscript>\r\n                </body>\r\n                </html>";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_IgnoreNoscriptElements(ignoreNoscriptElements);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.IgnoreNoscriptElements.pdf");
```

## Ver también

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
