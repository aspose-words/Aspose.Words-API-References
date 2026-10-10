---
title: "Aspose::Words::WatermarkType énum"
linktitle: "WatermarkType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::WatermarkType énum. Spécifie le type de filigrane en C++."
type: docs
weight: 131000
url: /fr/cpp/aspose.words/watermarktype/
---
## WatermarkType enum


Spécifie le type de filigrane.

```cpp
enum class WatermarkType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Texte | 0 | Indique que le texte sera utilisé comme filigrane. Un tel filigrane correspond à un objet WordArt. |
| Image | 1 | Indique que l'image sera utilisée comme filigrane. Un tel filigrane correspond à une forme contenant une image. |
| None | 2 | Indique que le filigrane n'est pas défini. |


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
