---
title: "Método SaveFormatToLoadFormat de Aspose::Words::FileFormatUtil"
linktitle: "SaveFormatToLoadFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método SaveFormatToLoadFormat de Aspose::Words::FileFormatUtil. Convierte un valor SaveFormat a un valor LoadFormat si es posible en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil::SaveFormatToLoadFormat method


Convierte un valor [SaveFormat](../../saveformat/) a un valor [LoadFormat](../../loadformat/) si es posible.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat saveFormat)
```


## Ejemplos



Muestra cómo convertir un formato de guardado a su formato de carga correspondiente.
```cpp
ASSERT_EQ(Aspose::Words::LoadFormat::Html, Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Html));

// Algunos tipos de archivo pueden tener documentos guardados, pero no cargados usando Aspose.Words.
// Si intentamos convertir un formato de guardado de ese tipo a un formato de carga, se lanzará una excepción.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Jpeg);
})(), System::ArgumentException);
```

## Ver también

* Enum [LoadFormat](../../loadformat/)
* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
