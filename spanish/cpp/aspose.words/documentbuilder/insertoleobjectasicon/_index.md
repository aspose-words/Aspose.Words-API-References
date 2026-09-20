---
title: "Método Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon"
linktitle: "InsertOleObjectAsIcon"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon. Inserta un objeto OLE incrustado como ícono desde un flujo en el documento. Permite especificar el archivo de ícono y el título. Detecta el tipo de objeto OLE usando el parámetro progID proporcionado en C++."
type: docs
weight: 42000
url: /es/cpp/aspose.words/documentbuilder/insertoleobjectasicon/
---
## DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) method


Inserta un objeto OLE incrustado como ícono desde un flujo en el documento. Permite especificar el archivo de ícono y el título. Detecta el tipo de objeto OLE usando el parámetro progID proporcionado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, const System::String &iconFile, const System::String &iconCaption)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | Flujo que contiene datos de la aplicación. |
| progId | const System::String\& | ProgId del objeto OLE. |
| iconFile | const System::String\& | Ruta completa al archivo ICO. Si el valor es **null**, Aspose.Words utilizará una imagen predefinida. |
| iconCaption | const System::String\& | Leyenda del ícono. Si el valor es **null**, Aspose.Words utilizará una leyenda de ícono predefinida. |

### ReturnValue

Nodo de forma que contiene el objeto Ole y se inserta en la posición actual del Builder.

## Ejemplos



Muestra cómo insertar un objeto OLE incrustado o vinculado como ícono en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
// el ícono según 'progId' y usa el nombre de archivo para la leyenda del ícono.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
    // el ícono según la extensión del archivo y usa el nombre de archivo para la leyenda del ícono.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, bool, const System::String\&, const System::String\&) method


Inserta un objeto OLE incrustado o vinculado como ícono en el documento. Permite especificar el archivo de ícono y el título. Detecta el tipo de objeto OLE usando la extensión del archivo.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | Ruta completa al archivo. |
| isLinked | bool | Si **true**, se inserta un objeto OLE vinculado; de lo contrario, se inserta un objeto OLE incrustado. |
| iconFile | const System::String\& | Ruta completa al archivo ICO. Si el valor es **null**, Aspose.Words utilizará una imagen predefinida. |
| iconCaption | const System::String\& | Leyenda del ícono. Si el valor es **null**, Aspose.Words utilizará el nombre del archivo. |

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
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) method


Inserta un objeto OLE incrustado o vinculado como ícono en el documento. Permite especificar el archivo de ícono y el título. Detecta el tipo de objeto OLE usando el parámetro progID proporcionado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, const System::String &progId, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | Ruta completa al archivo. |
| progId | const System::String\& | ProgId del objeto OLE. |
| isLinked | bool | Si **true**, se inserta un objeto OLE vinculado; de lo contrario, se inserta un objeto OLE incrustado. |
| iconFile | const System::String\& | Ruta completa al archivo ICO. Si el valor es **null**, Aspose.Words utilizará una imagen predefinida. |
| iconCaption | const System::String\& | Leyenda del ícono. Si el valor es **null**, Aspose.Words utilizará el nombre del archivo. |

### ReturnValue

Nodo de forma que contiene el objeto Ole y se inserta en la posición actual del Builder.

## Ejemplos



Muestra cómo insertar un objeto OLE incrustado o vinculado como ícono en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
// el ícono según 'progId' y usa el nombre de archivo para la leyenda del ícono.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
    // el ícono según la extensión del archivo y usa el nombre de archivo para la leyenda del ícono.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream<CharType, Traits> &stream, System::String progId, System::String iconFile, System::String iconCaption)
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
