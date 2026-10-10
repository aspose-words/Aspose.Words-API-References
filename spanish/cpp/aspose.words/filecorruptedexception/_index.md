---
title: "Aspose::Words::FileCorruptedException typedef"
linktitle: "FileCorruptedException"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::FileCorruptedException typedef. Lanzada durante la carga del documento, cuando el documento parece estar corrupto e imposible de cargar. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 133000
url: /es/cpp/aspose.words/filecorruptedexception/
---
## FileCorruptedException typedef


Lanzada durante la carga del documento, cuando el documento parece estar corrupto e imposible de cargar. Para obtener más información, visite el artículo de documentación [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
using Aspose::Words::FileCorruptedException = typedef System::ExceptionWrapper<Details_FileCorruptedException>
```


## Ejemplos



Muestra cómo capturar una FileCorruptedException.
```cpp
try
{
    // Si obtenemos un mensaje de error "Contenido ilegible" al intentar abrir un documento con Microsoft Word,
    // es probable que se lance una excepción al intentar cargar ese documento usando Aspose.Words.
    auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted document.docx");
}
catch (Aspose::Words::FileCorruptedException& e)
{
    std::cout << e->get_Message() << std::endl;
}
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
