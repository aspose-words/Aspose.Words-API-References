---
title: "Metodo Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort"
linktitle: "get_FitToViewPort"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort. Specifica se l'SVG di output deve riempire l'area disponibile del viewport (finestra del browser o contenitore). Quando impostato su true, larghezza e altezza dell'SVG di output sono impostate al 100%. Il valore predefinito è false in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/svgsaveoptions/get_fittoviewport/
---
## SvgSaveOptions::get_FitToViewPort method


Specifica se l'SVG di output deve riempire l'area disponibile del viewport (finestra del browser o contenitore). Quando impostato su **true**, larghezza e altezza dell'SVG di output sono impostate al 100%. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort() const
```


## Esempi



Mostra come imitare le proprietà delle immagini durante la conversione di un documento .docx in .svg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Configura l'oggetto SvgSaveOptions per salvare senza bordi di pagina o testo selezionabile.
auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.SaveLikeImage.svg", options);
```

## Vedi anche

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
