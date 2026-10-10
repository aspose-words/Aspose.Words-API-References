---
title: "Aspose::Words::Saving::SvgTextOutputMode enum"
linktitle: "SvgTextOutputMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::SvgTextOutputMode enum. Consente di specificare come il testo all'interno di un documento debba essere renderizzato quando si salva in formato SVG in C++."
type: docs
weight: 83000
url: /it/cpp/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enum


Consente di specificare come il testo all'interno di un documento deve essere renderizzato quando viene salvato in formato SVG.

```cpp
enum class SvgTextOutputMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| UseSvgFonts | 0 | I font SVG vengono utilizzati per renderizzare il testo. Nota, non tutti i browser supportano i font SVG. |
| UseTargetMachineFonts | 1 | [Fonts](../../aspose.words.fonts/) installati sulla macchina di destinazione vengono utilizzati per renderizzare il testo. Nota, se alcuni dei font utilizzati nel documento non sono disponibili sulla macchina di destinazione, il documento potrebbe apparire in modo diverso. |
| UsePlacedGlyphs | 2 | Il testo viene renderizzato usando curve. Nota, la selezione del testo non funzionerà se utilizzi questa opzione. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
