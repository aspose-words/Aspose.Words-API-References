---
title: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts méthode"
linktitle: "get_AllowEmbeddingPostScriptFonts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts méthode. Obtient ou définit une valeur booléenne indiquant s’il faut autoriser l’incorporation de polices avec des contours PostScript lors de l’incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est false en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/saveoptions/get_allowembeddingpostscriptfonts/
---
## SaveOptions::get_AllowEmbeddingPostScriptFonts method


Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts() const
```

## Remarques


Remarque : Word n’incorpore pas les polices PostScript, mais peut ouvrir des documents contenant des polices incorporées de ce type.

Cette option ne fonctionne que lorsque la propriété [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) de [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) est définie sur **true**.

## Exemples



Montre comment enregistrer le document avec une police PostScript.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"PostScriptFont");
builder->Writeln(u"Some text with PostScript font.");

// Chargez la police avec PostScript à utiliser dans le document.
auto otf = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(System::IO::File::ReadAllBytes(get_FontsDir() + u"AllegroOpen.otf"));
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({otf}));

// Incorporez des polices TrueType.
doc->get_FontInfos()->set_EmbedTrueTypeFonts(true);

// Autoriser l’incorporation de polices PostScript lors de l’incorporation de polices TrueType.
// Microsoft Word n’incorpore pas les polices PostScript, mais peut ouvrir des documents contenant des polices incorporées de ce type.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat::Docx);
saveOptions->set_AllowEmbeddingPostScriptFonts(true);

doc->Save(get_ArtifactsDir() + u"Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

## Voir aussi

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
