---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName method"
linktitle: "get_ResourceFileName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName Methode. Gibt den Dateinamen (ohne Pfad) zurück oder legt ihn fest, unter dem die Ressource in C++ gespeichert wird."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/resourcesavingargs/get_resourcefilename/
---
## ResourceSavingArgs::get_ResourceFileName method


Liest oder setzt den Dateinamen (ohne Pfad), in dem die Ressource gespeichert wird.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName() const
```

## Hinweise


Diese Eigenschaft ermöglicht es Ihnen, zu definieren, wie die Ressourcendateinamen beim Export zu festem Seiten-HTML, SVG oder Markdown erzeugt werden.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den Dateinamen, der von Aspose.Words erzeugt wurde. Sie können den Wert dieser Eigenschaft ändern, um die Ressource in einer anderen Datei zu speichern. Beachten Sie, dass Dateinamen eindeutig sein müssen.

Aspose.Words erzeugt beim Export zu festem Seiten-HTML, SVG oder Markdown-Format automatisch einen eindeutigen Dateinamen für jede Ressource. Wie der Ressourcendateiname erzeugt wird, hängt davon ab, ob Sie das Dokument in einer Datei oder in einem Stream speichern.

Beim Speichern eines Dokuments in einer Datei sieht der erzeugte Ressourcendateiname so aus: *%<document base file name>.<image number>.<extension>*.

Beim Speichern eines Dokuments in einem Stream sieht der erzeugte Ressourcendateiname so aus: *Aspose.Words.<document guid>.<image number>.<extension>*.

[ResourceFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [ResourcesFolder](../../htmlfixedsaveoptions/get_resourcesfolder/) or [ResourcesFolder](../../svgsaveoptions/get_resourcesfolder/) and [ResourcesFolderAlias](../../htmlfixedsaveoptions/get_resourcesfolderalias/) or [ResourcesFolderAlias](../../svgsaveoptions/get_resourcesfolderalias/) or [ImagesFolder](../../markdownsaveoptions/get_imagesfolder/) or [ImagesFolderAlias](../../markdownsaveoptions/get_imagesfolderalias/) properties.

## Siehe auch

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
