---
title: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts método"
linktitle: "get_AllowEmbeddingPostScriptFonts"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts método. Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento cuando se guarda. El valor predeterminado es false en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/saveoptions/get_allowembeddingpostscriptfonts/
---
## SaveOptions::get_AllowEmbeddingPostScriptFonts method


Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento cuando se guarda. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts() const
```

## Observaciones


Nota, Word no incrusta fuentes PostScript, pero puede abrir documentos con fuentes incrustadas de este tipo.

Esta opción solo funciona cuando la propiedad [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) de [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) está establecida en **true**.

## Ejemplos



Muestra cómo guardar el documento con una fuente PostScript.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"PostScriptFont");
builder->Writeln(u"Some text with PostScript font.");

// Cargue la fuente con PostScript para usarla en el documento.
auto otf = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(System::IO::File::ReadAllBytes(get_FontsDir() + u"AllegroOpen.otf"));
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({otf}));

// Incruste fuentes TrueType.
doc->get_FontInfos()->set_EmbedTrueTypeFonts(true);

// Permita incrustar fuentes PostScript al incrustar fuentes TrueType.
// Microsoft Word no incrusta fuentes PostScript, pero puede abrir documentos con fuentes incrustadas de este tipo.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat::Docx);
saveOptions->set_AllowEmbeddingPostScriptFonts(true);

doc->Save(get_ArtifactsDir() + u"Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

## Ver también

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
