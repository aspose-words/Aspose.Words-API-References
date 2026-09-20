---
title: "Aspose::Words::FileFormatUtil::LoadFormatToExtension method"
linktitle: "LoadFormatToExtension"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::FileFormatUtil::LoadFormatToExtension method. Convierte un valor enumerado de formato de carga en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil::LoadFormatToExtension method


Convierte un valor enumerado de formato de carga en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial.

```cpp
static System::String Aspose::Words::FileFormatUtil::LoadFormatToExtension(Aspose::Words::LoadFormat loadFormat)
```

## Observaciones


El valor [WordML](../../saveformat/) se convierte en ".wml".

## Ejemplos



Muestra cómo usar los métodos de [FileFormatUtil](../) para detectar el formato de un documento.
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

* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
