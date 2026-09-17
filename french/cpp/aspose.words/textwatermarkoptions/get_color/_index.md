---
title: "Aspose::Words::TextWatermarkOptions::get_Color méthode"
linktitle: "get_Color"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TextWatermarkOptions::get_Color méthode. Obtient ou définit la couleur de la police. La valeur par défaut est Silver en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/textwatermarkoptions/get_color/
---
## TextWatermarkOptions::get_Color method


Obtient ou définit la couleur de la police. La valeur par défaut est **Silver**.

```cpp
System::Drawing::Color Aspose::Words::TextWatermarkOptions::get_Color() const
```


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

* Class [TextWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
