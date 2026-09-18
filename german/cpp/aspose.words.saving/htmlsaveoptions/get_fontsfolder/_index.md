---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder Methode"
linktitle: "get_FontsFolder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder Methode. Gibt den physischen Ordner an, in dem Schriftarten beim Export eines Dokuments nach HTML gespeichert werden. Standard ist eine leere Zeichenkette in C++."
type: docs
weight: 33000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolder/
---
## HtmlSaveOptions::get_FontsFolder method


Gibt den physischen Ordner an, in dem Schriftarten beim Export eines Dokuments nach HTML gespeichert werden. Standardwert ist ein leerer String.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder() const
```

## Hinweise


Wenn Sie ein [Document](../../../aspose.words/document/) im HTML-Format speichern und [ExportFontResources](../get_exportfontresources/) auf **true** gesetzt ist, muss Aspose.Words die im Dokument verwendeten Schriftarten als eigenständige Dateien speichern. [FontsFolder](./) ermöglicht es Ihnen, anzugeben, wo die Schriftarten gespeichert werden sollen, und [FontsFolderAlias](../get_fontsfolderalias/) ermöglicht die Angabe, wie die Schriftart-URIs konstruiert werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words standardmäßig die Schriftarten im selben Ordner, in dem die Dokumentdatei gespeichert wird. Verwenden Sie [FontsFolder](./), um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einen Stream speichern, hat Aspose.Words keinen Ordner, in dem die Schriftarten gespeichert werden können, muss die Schriftarten jedoch dennoch irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner in der Eigenschaft [FontsFolder](./) angeben oder benutzerdefinierte Streams über den Ereignishandler [FontSavingCallback](../get_fontsavingcallback/) bereitstellen.

Wenn der von [FontsFolder](./) angegebene Ordner nicht existiert, wird er automatisch erstellt.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where fonts should be saved.

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
