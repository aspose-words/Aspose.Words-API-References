---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias metodo"
linktitle: "get_ImagesFolderAlias"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias metodo. Specifica il nome della cartella usata per costruire gli URI delle immagini scritti in un documento XAML. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolderalias/
---
## XamlFlowSaveOptions::get_ImagesFolderAlias method


Specifica il nome della cartella usata per costruire gli URI delle immagini scritti in un documento XAML. Il valore predefinito è una stringa vuota.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias() const
```

## Note


Quando salvi un [Document](../../../aspose.words/document/) in formato XAML, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi. [ImagesFolder](../get_imagesfolder/) ti consente di specificare dove verranno salvate le immagini e [ImagesFolderAlias](./) permette di specificare come verranno costruiti gli URI delle immagini.

Se [ImagesFolderAlias](./) non è una stringa vuota, l'URI dell'immagine scritto in XAML sarà *ImagesFolderAlias + <image file name>*.

Se [ImagesFolderAlias](./) è una stringa vuota, l'URI dell'immagine scritto in XAML sarà *ImagesFolder + <image file name>*.

Se [ImagesFolderAlias](./) è impostato a '.' (punto), il nome del file immagine verrà scritto in XAML senza percorso, indipendentemente dalle altre opzioni.

## Vedi anche

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
