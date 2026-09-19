---
title: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode metodo"
linktitle: "get_TextOutputMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode metodo. Ottiene o imposta un valore che determina come il testo deve essere renderizzato in SVG in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.saving/svgsaveoptions/get_textoutputmode/
---
## SvgSaveOptions::get_TextOutputMode method


Ottiene o imposta un valore che determina come il testo deve essere renderizzato in SVG.

```cpp
Aspose::Words::Saving::SvgTextOutputMode Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode() const
```

## Note


Usa questa proprietà per ottenere o impostare la modalità di come il testo all'interno di un documento deve essere renderizzato durante il salvataggio in formato SVG.

Il valore predefinito è [UseTargetMachineFonts](../../svgtextoutputmode/).

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

* Enum [SvgTextOutputMode](../../svgtextoutputmode/)
* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
