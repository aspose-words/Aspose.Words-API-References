---
title: "Aspose::Words::DocumentBuilder::InsertOleObject método"
linktitle: "InsertOleObject"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertOleObject método. Inserta un objeto OLE incrustado desde un flujo en el documento en C++."
type: docs
weight: 41000
url: /es/cpp/aspose.words/documentbuilder/insertoleobject/
---
## DocumentBuilder::InsertOleObject(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserta un objeto OLE incrustado desde un flujo en el documento.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | Flujo que contiene datos de la aplicación. |
| progId | const System::String\& | Identificador programático del objeto OLE. |
| asIcon | bool | Especifica el modo Icónico o Normal del objeto OLE que se inserta. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Presentación de imagen del objeto OLE. Si el valor es **null** Aspose.Words usará una de las imágenes predefinidas. |

### ReturnValue

Nodo de forma que contiene el objeto Ole y se inserta en la posición actual del Builder.

## Ejemplos



Muestra cómo usar el constructor de documentos para incrustar objetos OLE en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insertar una hoja de cálculo de Microsoft Excel desde el sistema de archivos local
// en el documento manteniendo su apariencia predeterminada.
{
    System::SharedPtr<System::IO::Stream> spreadsheetStream = System::IO::File::Open(get_MyDir() + u"Spreadsheet.xlsx", System::IO::FileMode::Open);
    builder->Writeln(u"Spreadsheet Ole object:");
    // Si se omite 'presentation' y se establece 'asIcon', este método sobrecargado selecciona
    // el ícono según 'progId' y usa la leyenda de ícono predefinida.
    builder->InsertOleObject(spreadsheetStream, u"OleObject.xlsx", false, nullptr);
}

// Insertar una presentación de Microsoft Powerpoint como objeto OLE.
// Esta vez, tendrá una imagen descargada de la web para un ícono.
{
    System::SharedPtr<System::IO::Stream> powerpointStream = System::IO::File::Open(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    System::ArrayPtr<uint8_t> imgBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

    {
        auto imageStream = System::MakeObject<System::IO::MemoryStream>(imgBytes);
        builder->InsertParagraph();
        builder->Writeln(u"Powerpoint Ole object:");
        builder->InsertOleObject(powerpointStream, u"OleObject.pptx", true, imageStream);
    }
}

// Haz doble clic en estos objetos en Microsoft Word para abrir
// los archivos vinculados usando sus respectivas aplicaciones.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjects.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserta un objeto OLE incrustado o vinculado desde un archivo en el documento. Detecta el tipo de objeto OLE usando la extensión del archivo.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | Ruta completa al archivo. |
| isLinked | bool | Si **true**, se inserta un objeto OLE vinculado; de lo contrario, se inserta un objeto OLE incrustado. |
| asIcon | bool | Especifica el modo Icónico o Normal del objeto OLE que se inserta. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Presentación de imagen del objeto OLE. Si el valor es **null** Aspose.Words usará una de las imágenes predefinidas. |

### ReturnValue

Nodo de forma que contiene el objeto Ole y se inserta en la posición actual del Builder.

## Ejemplos



Muestra cómo insertar un objeto OLE en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Los objetos OLE son enlaces a archivos en nuestro sistema de archivos local que pueden ser abiertos por otras aplicaciones instaladas.
// Al hacer doble clic en estas formas se lanzará la aplicación y luego se usará para abrir el objeto vinculado.
// Hay tres formas de usar el método InsertOleObject para insertar estas formas y configurar su apariencia.
// 1 -  Imagen tomada del sistema de archivos local:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // Si se omite 'presentation' y se establece 'asIcon', este método sobrecargado selecciona
    // el ícono según la extensión del archivo y usa el nombre de archivo para la leyenda del ícono.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// Si se omite 'presentation' y se establece 'asIcon', este método sobrecargado selecciona
// el ícono según 'progId' y usa el nombre de archivo para la leyenda del ícono.
// 2 -  Ícono basado en la aplicación que abrirá el objeto:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
// el ícono según 'progId' y usa la leyenda de ícono predefinida.
// 3 -  Ícono de imagen de 32 x 32 píxeles o menos del sistema de archivos local, con una leyenda personalizada:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserta un objeto OLE incrustado o vinculado desde un archivo en el documento. Detecta el tipo de objeto OLE usando el parámetro progID proporcionado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, const System::String &progId, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | Ruta completa al archivo. |
| progId | const System::String\& | ProgId del objeto OLE. |
| isLinked | bool | Si **true**, se inserta un objeto OLE vinculado; de lo contrario, se inserta un objeto OLE incrustado. |
| asIcon | bool | Especifica el modo Icónico o Normal del objeto OLE que se inserta. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Presentación de imagen del objeto OLE. Si el valor es **null** Aspose.Words usará una de las imágenes predefinidas. |

### ReturnValue

Nodo de forma que contiene el objeto Ole y se inserta en la posición actual del Builder.

## Ejemplos



Muestra cómo insertar un objeto OLE en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Los objetos OLE son enlaces a archivos en nuestro sistema de archivos local que pueden ser abiertos por otras aplicaciones instaladas.
// Al hacer doble clic en estas formas se lanzará la aplicación y luego se usará para abrir el objeto vinculado.
// Hay tres formas de usar el método InsertOleObject para insertar estas formas y configurar su apariencia.
// 1 -  Imagen tomada del sistema de archivos local:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // Si se omite 'presentation' y se establece 'asIcon', este método sobrecargado selecciona
    // el ícono según la extensión del archivo y usa el nombre de archivo para la leyenda del ícono.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// Si se omite 'presentation' y se establece 'asIcon', este método sobrecargado selecciona
// el ícono según 'progId' y usa el nombre de archivo para la leyenda del ícono.
// 2 -  Ícono basado en la aplicación que abrirá el objeto:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
// el ícono según 'progId' y usa la leyenda de ícono predefinida.
// 3 -  Ícono de imagen de 32 x 32 píxeles o menos del sistema de archivos local, con una leyenda personalizada:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(std::basic_istream<CharType, Traits> &stream, System::String progId, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, System::String progId, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
