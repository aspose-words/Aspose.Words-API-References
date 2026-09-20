---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding método"
linktitle: "get_Encoding"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding método. Especifica la codificación a usar al exportar a HTML. El valor predeterminado es new UTF8Encoding(true) (UTF-8 con BOM) en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/htmlfixedsaveoptions/get_encoding/
---
## HtmlFixedSaveOptions::get_Encoding method


Especifica la codificación a usar al exportar a HTML. El valor predeterminado es **new UTF8Encoding(true)** (UTF-8 con BOM).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding() const
```


## Ejemplos



Muestra cómo establecer qué codificación usar al exportar un documento a HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello World!");

// La codificación predeterminada es UTF-8. Si queremos representar nuestro documento usando una codificación diferente,
// podemos usar un objeto SaveOptions para establecer una codificación específica.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());

ASSERT_EQ(u"US-ASCII", htmlFixedSaveOptions->get_Encoding()->get_EncodingName());

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

## Ver también

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
