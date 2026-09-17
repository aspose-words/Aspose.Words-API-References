---
title: "Classe Aspose::Words::Watermark"
linktitle: "Filigrane"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Watermark. Représente une classe pour travailler avec le filigrane du document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 76000
url: /fr/cpp/aspose.words/watermark/
---
## Watermark class


Représente une classe pour travailler avec le filigrane du document. Pour en savoir plus, consultez l'article de documentation [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class Watermark : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Type](./get_type/)() | Obtient le type de filigrane. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Supprime le filigrane. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Ajoute un filigrane image dans le document. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane image dans le document. |
| [SetImage](./setimage/)(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane image dans le document. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane image dans le document. |
| [SetText](./settext/)(const System::String\&) | Ajoute un filigrane texte dans le document. |
| [SetText](./settext/)(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Ajoute un filigrane texte dans le document. |
| static [Type](./type/)() |  |

## Exemples



Montre comment créer un filigrane texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ajoutez un filigrane texte simple.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Si nous souhaitons modifier le formatage du texte en l'utilisant comme filigrane,
// nous pouvons le faire en passant un objet TextWatermarkOptions lors de la création du filigrane.
auto textWatermarkOptions = System::MakeObject<Aspose::Words::TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(Aspose::Words::WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// Nous pouvons supprimer un filigrane d'un document comme ceci.
if (doc->get_Watermark()->get_Type() == Aspose::Words::WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
