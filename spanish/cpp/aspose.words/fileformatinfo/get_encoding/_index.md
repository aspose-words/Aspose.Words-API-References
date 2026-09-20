---
title: "Aspose::Words::FileFormatInfo::get_Encoding método"
linktitle: "get_Encoding"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::FileFormatInfo::get_Encoding método. Obtiene la codificación detectada si es aplicable al formato actual del documento. Por el momento detecta la codificación solo para documentos HTML en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/fileformatinfo/get_encoding/
---
## FileFormatInfo::get_Encoding method


Obtiene la codificación detectada si es aplicable al formato del documento actual. En este momento solo detecta la codificación para documentos HTML.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::FileFormatInfo::get_Encoding() const
```


## Ejemplos



Muestra cómo detectar la codificación en un archivo html.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// La propiedad Encoding se usa solo cuando creamos un objeto FileFormatInfo para un documento html.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## Ver también

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
