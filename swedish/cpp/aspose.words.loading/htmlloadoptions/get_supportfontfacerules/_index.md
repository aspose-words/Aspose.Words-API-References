---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules metod"
linktitle: "get_SupportFontFaceRules"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules metod. Hämtar eller anger ett värde som indikerar om @font-face-regler ska stödjas och om deklarerade typsnitt ska laddas. Standardvärdet är false i C++."
type: docs
weight: 6500
url: /sv/cpp/aspose.words.loading/htmlloadoptions/get_supportfontfacerules/
---
## HtmlLoadOptions::get_SupportFontFaceRules method


Hämtar eller anger ett värde som indikerar om @font-face-regler ska stödjas och om deklarerade teckensnitt ska laddas. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules() const
```

## Anmärkningar


Om detta alternativ är aktiverat laddas typsnitt som deklarerats i @font-face-regler och bäddas in i det resulterande dokumentets typsnittsdefinitioner (se [FontInfos](../../../aspose.words/documentbase/get_fontinfos/)). Detta gör de laddade typsnitten tillgängliga för rendering men aktiverar inte automatiskt inbäddning av typsnitten vid sparande. För att spara dokumentet med de laddade typsnitten bör egenskapen [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) i samlingen [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) sättas till **true**.

Följande typsnittformat stöds: TTF, EOT och WOFF.

@font-face-regler stöds inte när SVG-bilder laddas.

## Exempel



Visar hur man laddar deklarerade \"@font-face\"-regler.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_SupportFontFaceRules(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Html with FontFace.html", loadOptions);

ASSERT_EQ(u"Squarish Sans CT Regular", doc->get_FontInfos()->idx_get(0)->get_Name());
```

## Se även

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
