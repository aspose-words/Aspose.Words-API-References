---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts método"
linktitle: "get_EmbedSystemFonts"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts método. Especifica si se deben incrustar o no fuentes del sistema en el documento. El valor predeterminado para esta propiedad es false. Esta opción funciona solo cuando la opción EmbedTrueTypeFonts está establecida en true en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.fonts/fontinfocollection/get_embedsystemfonts/
---
## FontInfoCollection::get_EmbedSystemFonts method


Especifica si se deben incrustar o no fuentes del sistema en el documento. El valor predeterminado para esta propiedad es **false**. Esta opción funciona solo cuando la opción [EmbedTrueTypeFonts](../get_embedtruetypefonts/) está establecida en **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts() const
```

## Observaciones


Establecer esta propiedad en **true** es útil si el usuario está en un sistema de Asia Oriental y desea crear un documento que sea legible para otros que no tengan fuentes para ese idioma en su sistema. Por ejemplo, un usuario en un sistema japonés podría optar por incrustar las fuentes en un documento para que el documento japonés sea legible en todos los sistemas.

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
