---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements Methode"
linktitle: "get_IgnoreNoscriptElements"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements Methode. Gibt einen Wert zurück oder legt ihn fest, der angibt, ob <noscript>-HTML-Elemente ignoriert werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.loading/htmlloadoptions/get_ignorenoscriptelements/
---
## HtmlLoadOptions::get_IgnoreNoscriptElements method


Liest oder setzt einen Wert, der angibt, ob <noscript>-HTML-Elemente ignoriert werden. Standardwert ist **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements() const
```


## Beispiele



Zeigt, wie man <noscript>-HTML-Elemente ignoriert.
```cpp
const System::String html = u"\r\n                <html>\r\n                  <head>\r\n                    <title>NOSCRIPT</title>\r\n                      <meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n                      <script type=\"text/javascript\">\r\n                        alert(\"Hello, world!\");\r\n                      </script>\r\n                  </head>\r\n                <body>\r\n                  <noscript><p>Your browser does not support JavaScript!</p></noscript>\r\n                </body>\r\n                </html>";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_IgnoreNoscriptElements(ignoreNoscriptElements);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.IgnoreNoscriptElements.pdf");
```

## Siehe auch

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
