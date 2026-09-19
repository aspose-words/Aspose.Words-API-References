---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules metodo"
linktitle: "get_SupportFontFaceRules"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules metodo. Ottiene o imposta un valore che indica se supportare le regole @font-face e se caricare i font dichiarati. Il valore predefinito è false in C++."
type: docs
weight: 6500
url: /it/cpp/aspose.words.loading/htmlloadoptions/get_supportfontfacerules/
---
## HtmlLoadOptions::get_SupportFontFaceRules method


Ottiene o imposta un valore che indica se supportare le regole @font-face e se caricare i font dichiarati. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules() const
```

## Note


Se questa opzione è abilitata, i font dichiarati nelle regole @font-face vengono caricati e incorporati nelle definizioni dei font del documento risultante (vedi [FontInfos](../../../aspose.words/documentbase/get_fontinfos/)). Questo rende i font caricati disponibili per il rendering ma non abilita automaticamente l'incorporamento dei font al salvataggio. Per salvare il documento con i font caricati, la proprietà [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) della collezione [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) dovrebbe essere impostata su **true**.

I formati di font supportati sono TTF, EOT e WOFF.

Le regole @font-face non sono supportate durante il caricamento di immagini SVG.

## Esempi



Mostra come caricare le regole "@font-face" dichiarate.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_SupportFontFaceRules(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Html with FontFace.html", loadOptions);

ASSERT_EQ(u"Squarish Sans CT Regular", doc->get_FontInfos()->idx_get(0)->get_Name());
```

## Vedi anche

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
