---
title: "Metodo Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName"
linktitle: "get_FallbackFontName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName. Nome del carattere che verrà utilizzato se non viene trovato alcun carattere previsto nelle collezioni della stampante e dei caratteri incorporati in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/pclsaveoptions/get_fallbackfontname/
---
## PclSaveOptions::get_FallbackFontName method


Nome del font che verrà utilizzato se non viene trovato alcun font previsto nella stampante e nelle raccolte di font integrati.

```cpp
System::String Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName() const
```


## Esempi



Mostra come dichiarare un carattere che una stampante applicherà al testo stampato come sostituto nel caso in cui il carattere originale non sia disponibile.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_FallbackFontName(u"Times New Roman");

// Questo documento istruirà la stampante ad applicare "Times New Roman" al testo con il carattere mancante.
// Se anche "Times New Roman" non fosse disponibile, la stampante utilizzerà come predefinito il carattere "Arial".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

## Vedi anche

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
