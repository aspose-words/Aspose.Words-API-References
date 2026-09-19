---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout metodo"
linktitle: "get_PageLayout"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout metodo. Ottiene o imposta il layout utilizzato durante il rendering di più pagine in un unico output in C++."
type: docs
weight: 9500
url: /it/cpp/aspose.words.saving/imagesaveoptions/get_pagelayout/
---
## ImageSaveOptions::get_PageLayout method


Ottiene o imposta il layout utilizzato durante il rendering di più pagine in un unico output.

```cpp
System::SharedPtr<Aspose::Words::Saving::MultiPageLayout> Aspose::Words::Saving::ImageSaveOptions::get_PageLayout() const
```

## Note


Utilizza uno dei metodi factory di [MultiPageLayout](../../multipagelayout/) per configurare questa proprietà.

Per [Tiff](../../../aspose.words/saveformat/) il valore predefinito è [TiffFrames](../../multipagelayout/tiffframes/). Per altri formati il valore predefinito è [SinglePage](../../multipagelayout/singlepage/).

Questa proprietà ha effetto solo durante il salvataggio nei seguenti formati: [Jpeg](../../../aspose.words/saveformat/), [Gif](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Tiff](../../../aspose.words/saveformat/), [WebP](../)

## Esempi



Mostra come salvare il documento in un'immagine JPG con le impostazioni di layout multipagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Configura un layout a griglia con:
// - 3 colonne per riga.
// - Spaziatura di 10pt tra le pagine (orizzontale e verticale).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Layout alternativi:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Personalizza lo sfondo e il bordo.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## Vedi anche

* Class [MultiPageLayout](../../multipagelayout/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
