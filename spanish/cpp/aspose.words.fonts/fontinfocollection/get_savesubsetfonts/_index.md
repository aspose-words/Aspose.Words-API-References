---
title: "Método Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts"
linktitle: "get_SaveSubsetFonts"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts. Especifica si se debe guardar o no un subconjunto de las fuentes TrueType incrustadas con el documento. El valor predeterminado para esta propiedad es false. Esta opción funciona solo cuando la propiedad EmbedTrueTypeFonts está establecida en true en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.fonts/fontinfocollection/get_savesubsetfonts/
---
## FontInfoCollection::get_SaveSubsetFonts method


Especifica si se debe guardar o no un subconjunto de las fuentes TrueType incrustadas con el documento. El valor predeterminado para esta propiedad es **false**. Esta opción funciona solo cuando la propiedad [EmbedTrueTypeFonts](../get_embedtruetypefonts/) está establecida en **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts() const
```


## Ejemplos



Muestra cómo guardar un documento con fuentes TrueType incrustadas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## Ver también

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
