---
title: "Aspose::Words::Rendering::NodeRendererBase::Save méthode"
linktitle: "Save"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Rendering::NodeRendererBase::Save méthode. Rend la forme en image et l’enregistre dans un flux en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.rendering/noderendererbase/save/
---
## NodeRendererBase::Save(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


Rend la forme dans une image et l'enregistre dans un flux.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::SharedPtr<System::IO::Stream> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Le flux où enregistrer l’image de la forme. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | Spécifie les options qui contrôlent la façon dont la forme est rendue et enregistrée. Peut être **null**. Si c’est **null**, l’image sera enregistrée au format PNG. |

## Exemples



Montre comment utiliser un rendu de forme pour exporter des formes vers des fichiers dans le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// Il y a 7 formes dans le document, dont une forme groupée avec 2 formes enfants.
// Nous rendrons chaque forme dans un fichier image dans le système de fichiers local
// tout en ignorant les formes de groupe puisqu'elles n'ont aucune apparence.
// Cela produira 6 fichiers image.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method


Rend la forme dans une image SVG et l'enregistre dans un flux.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::SharedPtr<System::IO::Stream> &stream, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Le flux où enregistrer l’image SVG de la forme. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\> | Spécifie les options qui contrôlent la façon dont la forme est rendue et enregistrée. Peut être **null**. Si c'est **null**, l'image sera enregistrée avec les options par défaut. |

## Exemples



Montre comment transmettre les options d'enregistrement lors du rendu des formules Office.
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

## Voir aussi

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


Rend la forme dans une image et l'enregistre dans un fichier.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::String &fileName, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le nom du fichier image. Si un fichier portant le nom spécifié existe déjà, le fichier existant est écrasé. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | Spécifie les options qui contrôlent la façon dont la forme est rendue et enregistrée. Peut être **null**. |

## Exemples



Montre comment rendre un objet Office [Math](../../../aspose.words.math/) en un fichier image dans le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Créez un objet "ImageSaveOptions" à transmettre à la méthode "Save" du rendu de nœud pour modifier
// la façon dont il rend le nœud OfficeMath en image.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Définissez la propriété "Scale" à 5 pour rendre l'objet à cinq fois sa taille originale.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method


Rend la forme dans une image SVG et l'enregistre dans un fichier.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::String &fileName, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le nom du fichier image. Si un fichier portant le nom spécifié existe déjà, le fichier existant est écrasé. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\> | Spécifie les options qui contrôlent la façon dont la forme est rendue et enregistrée. Peut être **null**. |

## Exemples



Montre comment transmettre les options d'enregistrement lors du rendu des formules Office.
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

## Voir aussi

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Rendering::NodeRendererBase::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```

## Voir aussi

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Rendering::NodeRendererBase::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```

## Voir aussi

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
