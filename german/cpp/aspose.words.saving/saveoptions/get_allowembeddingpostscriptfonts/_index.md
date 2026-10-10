---
title: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts Methode"
linktitle: "get_AllowEmbeddingPostScriptFonts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts Methode. Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, ob das Einbetten von Schriften mit PostScript-Umrissen beim Einbetten von TrueType-Schriften in ein Dokument beim Speichern erlaubt ist. Der Standardwert ist false in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/saveoptions/get_allowembeddingpostscriptfonts/
---
## SaveOptions::get_AllowEmbeddingPostScriptFonts method


Liest oder setzt einen booleschen Wert, der angibt, ob das Einbetten von Schriften mit PostScript-Umrissen beim Einbetten von TrueType-Schriften in ein Dokument beim Speichern erlaubt ist. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts() const
```

## Hinweise


Hinweis: Word bettet keine PostScript-Schriften ein, kann jedoch Dokumente mit eingebetteten Schriften dieses Typs öffnen.

Diese Option funktioniert nur, wenn die Eigenschaft [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) der [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) auf **true** gesetzt ist.

## Beispiele



Zeigt, wie das Dokument mit einer PostScript-Schrift gespeichert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"PostScriptFont");
builder->Writeln(u"Some text with PostScript font.");

// Laden Sie die Schrift mit PostScript, um sie im Dokument zu verwenden.
auto otf = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(System::IO::File::ReadAllBytes(get_FontsDir() + u"AllegroOpen.otf"));
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({otf}));

// TrueType-Schriften einbetten.
doc->get_FontInfos()->set_EmbedTrueTypeFonts(true);

// Einbetten von PostScript-Schriften beim Einbetten von TrueType-Schriften erlauben.
// Microsoft Word bettet keine PostScript-Schriften ein, kann jedoch Dokumente mit eingebetteten Schriften dieses Typs öffnen.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat::Docx);
saveOptions->set_AllowEmbeddingPostScriptFonts(true);

doc->Save(get_ArtifactsDir() + u"Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

## Siehe auch

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
