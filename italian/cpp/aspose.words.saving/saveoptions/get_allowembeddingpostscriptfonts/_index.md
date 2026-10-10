---
title: "metodo Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts"
linktitle: "get_AllowEmbeddingPostScriptFonts"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts. Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di caratteri con contorni PostScript quando si incorporano caratteri TrueType in un documento al momento del salvataggio. Il valore predefinito è false in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/saveoptions/get_allowembeddingpostscriptfonts/
---
## SaveOptions::get_AllowEmbeddingPostScriptFonts method


Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts() const
```

## Note


Nota, Word non incorpora caratteri PostScript, ma può aprire documenti con caratteri incorporati di questo tipo.

Questa opzione funziona solo quando la proprietà [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) di [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) è impostata su **true**.

## Esempi



Mostra come salvare il documento con un carattere PostScript.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"PostScriptFont");
builder->Writeln(u"Some text with PostScript font.");

// Carica il carattere con PostScript da utilizzare nel documento.
auto otf = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(System::IO::File::ReadAllBytes(get_FontsDir() + u"AllegroOpen.otf"));
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({otf}));

// Incorpora caratteri TrueType.
doc->get_FontInfos()->set_EmbedTrueTypeFonts(true);

// Consenti l'incorporamento di caratteri PostScript durante l'incorporamento di caratteri TrueType.
// Microsoft Word non incorpora caratteri PostScript, ma può aprire documenti con caratteri incorporati di questo tipo.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat::Docx);
saveOptions->set_AllowEmbeddingPostScriptFonts(true);

doc->Save(get_ArtifactsDir() + u"Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

## Vedi anche

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
