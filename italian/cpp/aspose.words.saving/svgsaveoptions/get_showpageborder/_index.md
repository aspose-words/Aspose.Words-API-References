---
title: "Metodo Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder"
linktitle: "get_ShowPageBorder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder. Controlla se un bordo viene aggiunto al contorno della pagina. Il valore predefinito è true in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.saving/svgsaveoptions/get_showpageborder/
---
## SvgSaveOptions::get_ShowPageBorder method


Controlla se un bordo viene aggiunto al contorno della pagina. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder() const
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
