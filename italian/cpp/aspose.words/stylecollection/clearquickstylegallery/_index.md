---
title: "Aspose::Words::StyleCollection::ClearQuickStyleGallery metodo"
linktitle: "ClearQuickStyleGallery"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::StyleCollection::ClearQuickStyleGallery metodo. Rimuove tutti gli stili dal pannello Quick Style Gallery in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection::ClearQuickStyleGallery method


Rimuove tutti gli stili dal pannello Quick [Style](../../style/) Gallery.

```cpp
void Aspose::Words::StyleCollection::ClearQuickStyleGallery()
```


## Esempi



Mostra come rimuovere gli stili dal pannello [Style](../../style/) Gallery.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
// Nota che la rimozione degli stili funziona solo con il formato DOCX per ora.
doc->get_Styles()->ClearQuickStyleGallery();

doc->Save(get_ArtifactsDir() + u"Styles.RemoveStylesFromStyleGallery.docx");
```

## Vedi anche

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
