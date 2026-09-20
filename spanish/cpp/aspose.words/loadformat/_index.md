---
title: "Aspose::Words::LoadFormat enumeración"
linktitle: "LoadFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::LoadFormat enum. Indica el formato del documento que se debe cargar en C++."
type: docs
weight: 97000
url: /es/cpp/aspose.words/loadformat/
---
## LoadFormat enum


Indica el formato del documento que se va a cargar.

```cpp
enum class LoadFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | 0 | Instruye a Aspose.Words a reconocer el formato automáticamente. |
| MsWorks | 8 | Microsoft Works 8 [Documento](../document/). |
| Doc | 10 | Microsoft Word 95 o Word 97 - 2003 [Documento](../document/). |
| Dot | 11 | Plantilla de Microsoft Word 95 o Word 97 - 2003. |
| DocPreWord60 | 12 | El documento está en formato pre-Word 95. Aspose.Words no admite actualmente la carga de dichos documentos. |
| Docx | 20 | Office Open XML WordprocessingML [Documento](../document/) (sin macros). |
| Docm | 21 | Office Open XML WordprocessingML con macros habilitadas [Documento](../document/). |
| Dotx | 22 | Plantilla de Office Open XML WordprocessingML (sin macros). |
| Dotm | 23 | Plantilla de Office Open XML WordprocessingML con macros habilitadas. |
| FlatOpc | 24 | Office Open XML WordprocessingML almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcMacroEnabled | 25 | Office Open XML WordprocessingML con macros habilitadas [Documento](../document/) almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcTemplate | 26 | Plantilla de Office Open XML WordprocessingML (sin macros) almacenada en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcTemplateMacroEnabled | 27 | Plantilla de Office Open XML WordprocessingML con macros habilitadas almacenada en un archivo XML plano en lugar de un paquete ZIP. |
| Rtf | 30 | Formato RTF. |
| WordML | 31 | Formato WordprocessingML de Microsoft Word 2003. |
| Html | 50 | Formato HTML. |
| Mhtml | 51 | Formato MHTML (archivo web). |
| Mobi | 52 | Formato MOBI. Utilizado por el lector MobiPocket y los lectores Amazon Kindle. |
| Chm | 53 | Formato CHM (Ayuda HTML compilada). |
| Azw3 | 54 | Formato AZW3. Utilizado por los lectores Amazon Kindle. |
| Epub | 55 | Formato EPUB. |
| Odt | 60 | Texto ODF [Documento](../document/). |
| Ott | 61 | Plantilla de Texto ODF [Documento](../document/). |
| Text | 62 | Texto sin formato. |
| Markdown | 63 | Documento de texto Markdown. |
| Xml | 65 | Documento XML. |
| Unknown | 255 | Formato no reconocido, no se puede cargar con [Aspose.Words](../). |


## Ejemplos



Muestra cómo usar los métodos de [FileFormatUtil](../fileformatutil/) para detectar el formato de un documento.
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


Muestra cómo especificar una URI base al abrir un documento html.
```cpp
// Supongamos que queremos cargar un documento .html que contiene una imagen vinculada mediante una URI relativa
// mientras la imagen está en una ubicación diferente. En ese caso, necesitaremos resolver la URI relativa en una absoluta.
// Podemos proporcionar una URI base usando un objeto HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Aunque la imagen estaba rota en el .html de entrada, nuestra URI base personalizada nos ayudó a reparar el enlace.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Este documento de salida mostrará la imagen que faltaba.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
