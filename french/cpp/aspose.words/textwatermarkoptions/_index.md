---
title: "Aspose::Words::TextWatermarkOptions classe"
linktitle: "TextWatermarkOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TextWatermarkOptions classe. Contient des options qui peuvent être spécifiées lors de l'ajout d'un filigrane texte. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 72000
url: /fr/cpp/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class


Contient des options qui peuvent être spécifiées lors de l'ajout d'un filigrane avec du texte. Pour en savoir plus, consultez l'article de documentation [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class TextWatermarkOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Color](./get_color/)() const | Obtient ou définit la couleur de la police. La valeur par défaut est **Silver**. |
| [get_FontFamily](./get_fontfamily/)() const | Obtient ou définit le nom de la famille de police. La valeur par défaut est "Calibri". |
| [get_FontSize](./get_fontsize/)() const | Obtient ou définit une taille de police. La valeur par défaut est 0 - auto. |
| [get_IsSemitrasparent](./get_issemitrasparent/)() const | Obtient ou définit une valeur booléenne qui détermine l'opacité du filigrane. La valeur par défaut est **true**. |
| [get_Layout](./get_layout/)() const | Obtient ou définit la disposition du filigrane. La valeur par défaut est [Diagonal](../watermarklayout/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::TextWatermarkOptions::get_Color](./get_color/). |
| [set_FontFamily](./set_fontfamily/)(const System::String\&) | Définisseur pour [Aspose::Words::TextWatermarkOptions::get_FontFamily](./get_fontfamily/). |
| [set_FontSize](./set_fontsize/)(float) | Définisseur pour [Aspose::Words::TextWatermarkOptions::get_FontSize](./get_fontsize/). |
| [set_IsSemitrasparent](./set_issemitrasparent/)(bool) | Définisseur pour [Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent](./get_issemitrasparent/). |
| [set_Layout](./set_layout/)(Aspose::Words::WatermarkLayout) | Définisseur pour [Aspose::Words::TextWatermarkOptions::get_Layout](./get_layout/). |
| [TextWatermarkOptions](./textwatermarkoptions/)() |  |
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
