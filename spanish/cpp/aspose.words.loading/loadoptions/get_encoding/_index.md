---
title: "Método Aspose::Words::Loading::LoadOptions::get_Encoding"
linktitle: "get_Encoding"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::LoadOptions::get_Encoding. Obtiene o establece la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. Puede ser null. El valor predeterminado es null en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.loading/loadoptions/get_encoding/
---
## LoadOptions::get_Encoding method


Obtiene o establece la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. Puede ser **null**. El valor predeterminado es **null**.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Loading::LoadOptions::get_Encoding() const
```

## Observaciones


Esta propiedad se usa solo al cargar documentos HTML, TXT o CHM.

Si la codificación no está especificada dentro del documento y esta propiedad es **null**, el sistema intentará detectar automáticamente la codificación.

## Ejemplos



Muestra cómo establecer la codificación con la que abrir un documento.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Encoding(System::Text::Encoding::get_ASCII());

// Cargue el documento pasando el objeto LoadOptions, luego verifique el contenido del documento.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_TRUE(doc->ToString(Aspose::Words::SaveFormat::Text).Contains(u"This is a sample text in English."));
```

## Ver también

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
