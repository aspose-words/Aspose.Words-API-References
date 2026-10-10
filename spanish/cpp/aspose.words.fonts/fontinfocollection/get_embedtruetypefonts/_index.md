---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts método"
linktitle: "get_EmbedTrueTypeFonts"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts método. Especifica si se deben incrustar o no fuentes TrueType en un documento cuando se guarda. El valor predeterminado para esta propiedad es false en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/
---
## FontInfoCollection::get_EmbedTrueTypeFonts method


Especifica si se deben incrustar fuentes TrueType en un documento al guardarlo. El valor predeterminado para esta propiedad es **false**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts() const
```

## Observaciones


Incrustar fuentes TrueType permite a otros ver el documento con las mismas fuentes que se usaron para crearlo, pero puede aumentar sustancialmente el tamaño del documento.

Esta opción funciona solo para los formatos DOC, DOCX y RTF.

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
