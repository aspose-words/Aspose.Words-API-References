---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules método"
linktitle: "get_SupportFontFaceRules"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules método. Obtiene o establece un valor que indica si se deben admitir reglas @font-face y si se deben cargar fuentes declaradas. El valor predeterminado es false en C++."
type: docs
weight: 6500
url: /es/cpp/aspose.words.loading/htmlloadoptions/get_supportfontfacerules/
---
## HtmlLoadOptions::get_SupportFontFaceRules method


Obtiene o establece un valor que indica si se deben admitir reglas @font-face y si se deben cargar las fuentes declaradas. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules() const
```

## Observaciones


Si esta opción está habilitada, las fuentes declaradas en reglas @font-face se cargan e incrustan en las definiciones de fuentes del documento resultante (ver [FontInfos](../../../aspose.words/documentbase/get_fontinfos/)). Esto hace que las fuentes cargadas estén disponibles para el renderizado, pero no habilita automáticamente la incrustación de las fuentes al guardar. Para guardar el documento con las fuentes cargadas, la propiedad [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) de la colección [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) debe establecerse en **true**.

Los formatos de fuente compatibles son TTF, EOT y WOFF.

Las reglas @font-face no son compatibles al cargar imágenes SVG.

## Ejemplos



Muestra cómo cargar reglas "@font-face" declaradas.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_SupportFontFaceRules(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Html with FontFace.html", loadOptions);

ASSERT_EQ(u"Squarish Sans CT Regular", doc->get_FontInfos()->idx_get(0)->get_Name());
```

## Ver también

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
