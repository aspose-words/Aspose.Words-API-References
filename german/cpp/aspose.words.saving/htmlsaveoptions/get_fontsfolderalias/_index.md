---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias Methode"
linktitle: "get_FontsFolderAlias"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias Methode. Gibt den Namen des Ordners an, der zum Erstellen von Schriftart-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Standard ist ein leerer String in C++."
type: docs
weight: 34000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolderalias/
---
## HtmlSaveOptions::get_FontsFolderAlias method


Gibt den Namen des Ordners an, der zum Erstellen von Schriftart-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Standardwert ist ein leerer String.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias() const
```

## Hinweise


Wenn Sie ein [Document](../../../aspose.words/document/) im HTML-Format speichern und [ExportFontResources](../get_exportfontresources/) auf **true** gesetzt ist, muss Aspose.Words die im Dokument verwendeten Schriftarten als eigenständige Dateien speichern. [FontsFolder](../get_fontsfolder/) ermöglicht es Ihnen, anzugeben, wo die Schriftarten gespeichert werden sollen, und [FontsFolderAlias](./) ermöglicht die Angabe, wie die Schriftart-URIs konstruiert werden.

Wenn [FontsFolderAlias](./) kein leerer String ist, wird die in HTML geschriebene Schriftart-URI *FontsFolderAlias + <font file name>* sein.

Wenn [FontsFolderAlias](./) ein leerer String ist, wird die in HTML geschriebene Schriftart-URI *FontsFolder + <font file name>* sein.

Wenn [FontsFolderAlias](./) auf '.' (Punkt) gesetzt ist, wird der Schriftartdateiname in HTML ohne Pfad geschrieben, unabhängig von anderen Optionen.

Eine alternative Möglichkeit, den Namen des Ordners zum Erstellen von Schriftart-URIs anzugeben, besteht darin, [ResourceFolderAlias](../get_resourcefolderalias/) zu verwenden.

## Beispiele



Zeigt, wie Ordner und Ordner‑Aliase für extern gespeicherte Ressourcen festgelegt werden, die Aspose.Words beim Speichern eines Dokuments nach HTML erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_ImageResolution(72);
options->set_FontResourcesSubsettingSizeThreshold(0);
options->set_FontsFolder(get_ArtifactsDir() + u"Fonts");
options->set_ImagesFolder(get_ArtifactsDir() + u"Images");
options->set_ResourceFolder(get_ArtifactsDir() + u"Resources");
options->set_FontsFolderAlias(u"http://example.com/fonts");
options->set_ImagesFolderAlias(u"http://example.com/images");
options->set_ResourceFolderAlias(u"http://example.com/resources");
options->set_ExportOriginalUrlForLinkedImages(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FolderAlias.html", options);
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
