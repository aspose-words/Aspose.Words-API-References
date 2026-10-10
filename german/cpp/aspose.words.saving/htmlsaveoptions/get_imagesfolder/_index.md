---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder Methode"
linktitle: "get_ImagesFolder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder Methode. Gibt den physischen Ordner an, in dem Bilder beim Export eines Dokuments in das HTML-Format gespeichert werden. Standard ist ein leerer String in C++."
type: docs
weight: 38000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolder/
---
## HtmlSaveOptions::get_ImagesFolder method


Gibt den physischen Ordner an, in dem Bilder beim Exportieren eines Dokuments ins HTML-Format gespeichert werden. Standard ist ein leerer String.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder() const
```

## Hinweise


Wenn Sie ein [Document](../../../aspose.words/document/) im HTML-Format speichern, muss Aspose.Words alle im Dokument eingebetteten Bilder als eigenständige Dateien speichern. [ImagesFolder](./) ermöglicht es Ihnen, anzugeben, wo die Bilder gespeichert werden sollen, und [ImagesFolderAlias](../get_imagesfolderalias/) ermöglicht die Angabe, wie die Bild-URIs konstruiert werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words standardmäßig die Bilder im selben Ordner, in dem die Dokumentdatei gespeichert wird. Verwenden Sie [ImagesFolder](./), um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einen Stream speichern, hat Aspose.Words keinen Ordner, in dem die Bilder gespeichert werden können, muss die Bilder jedoch dennoch irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner in der Eigenschaft [ImagesFolder](./) angeben oder benutzerdefinierte Streams über den Ereignishandler [ImageSavingCallback](../get_imagesavingcallback/) bereitstellen.

Wenn der von [ImagesFolder](./) angegebene Ordner nicht existiert, wird er automatisch erstellt.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where images should be saved.

## Beispiele



Zeigt, wie man den Ordner zum Speichern verknüpfter Bilder nach dem Speichern als .html angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Setzt eine Option, um Formularfelder als Klartext anstelle von HTML-Eingabeelementen zu exportieren.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
