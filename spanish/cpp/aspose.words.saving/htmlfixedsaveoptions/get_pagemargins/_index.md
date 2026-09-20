---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins método"
linktitle: "get_PageMargins"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins método. Especifica los márgenes alrededor de las páginas en un documento HTML. El valor de los márgenes se mide en puntos y debe ser igual o mayor que 0. El valor predeterminado es 10 puntos en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagemargins/
---
## HtmlFixedSaveOptions::get_PageMargins method


Especifica los márgenes alrededor de las páginas en un documento HTML. El valor de los márgenes se mide en puntos y debe ser igual o mayor que 0. El valor predeterminado es 10 puntos.

```cpp
double Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins() const
```

## Observaciones


Depende del valor de la propiedad [PageHorizontalAlignment](../get_pagehorizontalalignment/):

* Defines top, bottom and left page margins if the value is [Left](../../htmlfixedpagehorizontalalignment/).
* Defines top, bottom and right page margins if the value is [Right](../../htmlfixedpagehorizontalalignment/).
* Defines top and bottom page margins if the value is [Center](../../htmlfixedpagehorizontalalignment/).



## Ejemplos



Muestra cómo ajustar los márgenes de página al guardar un documento en HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_PageMargins(15);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins/styles.css");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }")->get_Success());
```

## Ver también

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
