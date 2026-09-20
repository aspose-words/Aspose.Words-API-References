---
title: "Aspose::Words::Drawing::OleFormat::get_SourceFullName método"
linktitle: "get_SourceFullName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::OleFormat::get_SourceFullName método. Obtiene o establece la ruta y el nombre del archivo fuente para el objeto OLE vinculado en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.drawing/oleformat/get_sourcefullname/
---
## OleFormat::get_SourceFullName method


Obtiene o establece la ruta y el nombre del archivo fuente para el objeto OLE vinculado.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SourceFullName()
```

## Observaciones


El valor predeterminado es una cadena vacía.

Si [SourceFullName](./) no es una cadena vacía, el objeto OLE está vinculado.

## Ejemplos



Muestra cómo insertar objetos OLE vinculados y no vinculados.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Incrusta un dibujo de Microsoft Visio en el documento como un objeto OLE.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", false, false, nullptr);

// Inserta un vínculo al archivo en el sistema de archivos local y muéstralo como un ícono.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", true, true, nullptr);

// Insertar objetos OLE crea formas que almacenan estos objetos.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());
ASSERT_EQ(2, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::OleObject;
}))));

// Si una forma contiene un objeto OLE, tendrá una propiedad "OleFormat" válida,
// que podemos usar para verificar algunos aspectos de la forma.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shapes[0]->get_OleFormat();

ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(false, oleFormat->get_OleIcon());

oleFormat = shapes[1]->get_OleFormat();

ASPOSE_ASSERT_EQ(true, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(true, oleFormat->get_OleIcon());

ASSERT_TRUE(oleFormat->get_SourceFullName().EndsWith(System::String(u"Images") + System::IO::Path::DirectorySeparatorChar + u"Microsoft Visio drawing.vsd"));
ASSERT_EQ(u"", oleFormat->get_SourceItem());

ASSERT_EQ(u"Microsoft Visio drawing.vsd", oleFormat->get_IconCaption());

doc->Save(get_ArtifactsDir() + u"Shape.OleLinks.docx");

// Si el objeto contiene datos OLE, podemos acceder a ellos mediante un flujo.
{
    System::SharedPtr<System::IO::MemoryStream> stream = oleFormat->GetOleEntry(u"\x0001" u"CompObj");
    System::ArrayPtr<uint8_t> oleEntryBytes = stream->ToArray();
    ASSERT_EQ(76, oleEntryBytes->get_Length());
}
```

## Ver también

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
