---
title: "Aspose::Words::Rendering::NodeRendererBase::Save método"
linktitle: "Save"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Rendering::NodeRendererBase::Save método. Renderiza la forma en una imagen y la guarda en un flujo en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.rendering/noderendererbase/save/
---
## NodeRendererBase::Save(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


Renderiza la forma en una imagen y la guarda en un flujo.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::SharedPtr<System::IO::Stream> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | El flujo donde guardar la imagen de la forma. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | Especifica las opciones que controlan cómo se renderiza y guarda la forma. Puede ser **null**. Si es **null**, la imagen se guardará en formato PNG. |

## Ejemplos



Muestra cómo usar un renderizador de formas para exportar formas a archivos en el sistema de archivos local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// Hay 7 formas en el documento, incluyendo una forma de grupo con 2 formas secundarias.
// Renderizaremos cada forma a un archivo de imagen en el sistema de archivos local
// mientras se ignoran los grupos de formas ya que no tienen apariencia.
// Esto producirá 6 archivos de imagen.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method


Renderiza la forma en una imagen SVG y la guarda en un flujo.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::SharedPtr<System::IO::Stream> &stream, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | El flujo donde guardar la imagen SVG de la forma. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\> | Especifica las opciones que controlan cómo se renderiza y guarda la forma. Puede ser **null**. Si es **null**, la imagen se guardará con las opciones predeterminadas. |

## Ejemplos



Muestra cómo pasar opciones de guardado al renderizar matemáticas de Office.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"SvgSaveOptions.Output.svg", options);

{
    auto stream = System::MakeObject<System::IO::MemoryStream>();
    math->GetMathRenderer()->Save(stream, options);
}
```

## Ver también

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


Renderiza la forma en una imagen y la guarda en un archivo.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::String &fileName, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El nombre del archivo de imagen. Si ya existe un archivo con el nombre especificado, se sobrescribe el archivo existente. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | Especifica las opciones que controlan cómo se renderiza y guarda la forma. Puede ser **null**. |

## Ejemplos



Muestra cómo renderizar un objeto de Office [Math](../../../aspose.words.math/) en un archivo de imagen en el sistema de archivos local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Cree un objeto "ImageSaveOptions" para pasar al método "Save" del renderizador de nodos y modificar
// cómo renderiza el nodo OfficeMath en una imagen.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Establezca la propiedad "Scale" a 5 para renderizar el objeto a cinco veces su tamaño original.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method


Renderiza la forma en una imagen SVG y la guarda en un archivo.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::String &fileName, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El nombre del archivo de imagen. Si ya existe un archivo con el nombre especificado, se sobrescribe el archivo existente. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\> | Especifica las opciones que controlan cómo se renderiza y guarda la forma. Puede ser **null**. |

## Ejemplos



Muestra cómo pasar opciones de guardado al renderizar matemáticas de Office.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"SvgSaveOptions.Output.svg", options);

{
    auto stream = System::MakeObject<System::IO::MemoryStream>();
    math->GetMathRenderer()->Save(stream, options);
}
```

## Ver también

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Rendering::NodeRendererBase::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Rendering::NodeRendererBase::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```

## Ver también

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
