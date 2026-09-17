---
title: "Aspose::Words::TextWatermarkOptions::get_Layout méthode"
linktitle: "get_Layout"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TextWatermarkOptions::get_Layout méthode. Obtient ou définit la disposition du filigrane. La valeur par défaut est Diagonal en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/textwatermarkoptions/get_layout/
---
## TextWatermarkOptions::get_Layout method


Obtient ou définit la disposition du filigrane. La valeur par défaut est [Diagonal](../../watermarklayout/).

```cpp
Aspose::Words::WatermarkLayout Aspose::Words::TextWatermarkOptions::get_Layout() const
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

* Enum [WatermarkLayout](../../watermarklayout/)
* Class [TextWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
