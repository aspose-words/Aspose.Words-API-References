---
title: "Método Aspose::Words::Document::get_OriginalFileName"
linktitle: "get_OriginalFileName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_OriginalFileName método. Obtiene el nombre de archivo original del documento en C++."
type: docs
weight: 40000
url: /es/cpp/aspose.words/document/get_originalfilename/
---
## Document::get_OriginalFileName method


Obtiene el nombre de archivo original del documento.

```cpp
System::String Aspose::Words::Document::get_OriginalFileName() const
```

## Observaciones


Devuelve **null** si el documento se cargó desde un flujo o se creó en blanco.

## Ejemplos



Muestra cómo obtener los detalles de la operación de carga de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```


Muestra cómo usar los métodos de [FileFormatUtil](../../fileformatutil/) para detectar el formato de un documento.
```cpp
// Cargue un documento desde un archivo que no tiene extensión y luego detecte su formato de archivo.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // A continuación se presentan dos métodos para convertir un LoadFormat a su SaveFormat correspondiente.
    // 1 - Obtenga la cadena de extensión de archivo para el LoadFormat y luego obtenga el SaveFormat correspondiente a partir de esa cadena:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 - Convierta directamente el LoadFormat a su SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Cargue un documento desde el flujo y luego guárdelo con la extensión de archivo detectada automáticamente.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
