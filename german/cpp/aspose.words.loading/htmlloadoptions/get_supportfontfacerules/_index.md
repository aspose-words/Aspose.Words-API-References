---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules Methode"
linktitle: "get_SupportFontFaceRules"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules Methode. Gibt einen Wert zurück oder legt ihn fest, der angibt, ob @font-face-Regeln unterstützt werden und ob deklarierte Schriften geladen werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 6500
url: /de/cpp/aspose.words.loading/htmlloadoptions/get_supportfontfacerules/
---
## HtmlLoadOptions::get_SupportFontFaceRules method


Liest oder setzt einen Wert, der angibt, ob @font-face‑Regeln unterstützt und deklarierte Schriften geladen werden sollen. Standardwert ist **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules() const
```

## Hinweise


Wenn diese Option aktiviert ist, werden in @font-face-Regeln deklarierte Schriften geladen und in die Schriftdefinitionen des resultierenden Dokuments eingebettet (siehe [FontInfos](../../../aspose.words/documentbase/get_fontinfos/)). Dadurch stehen die geladenen Schriften für das Rendern zur Verfügung, jedoch wird das Einbetten der Schriften beim Speichern nicht automatisch aktiviert. Um das Dokument mit den geladenen Schriften zu speichern, sollte die Eigenschaft [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) der Sammlung [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) auf **true** gesetzt werden.

Unterstützte Schriftformate sind TTF, EOT und WOFF.

@font-face-Regeln werden beim Laden von SVG-Bildern nicht unterstützt.

## Beispiele



Zeigt, wie deklarierte "@font-face"-Regeln geladen werden.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_SupportFontFaceRules(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Html with FontFace.html", loadOptions);

ASSERT_EQ(u"Squarish Sans CT Regular", doc->get_FontInfos()->idx_get(0)->get_Name());
```

## Siehe auch

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
