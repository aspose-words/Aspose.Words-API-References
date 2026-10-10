---
title: "Aspose::Words::Drawing::ShadowType enum"
linktitle: "ShadowType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShadowType enum. Anger typen av en formskugga i C++."
type: docs
weight: 35000
url: /sv/cpp/aspose.words.drawing/shadowtype/
---
## ShadowType enum


Anger typen av en formskugga.

```cpp
enum class ShadowType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| ShadowMixed | -2 | Ingen av de fördefinierade skuggförinställningarna. |
| Shadow1 | 1 | Första skuggtypen. |
| Shadow10 | 10 | Tionde skuggtypen. |
| Shadow11 | 11 | Elfte skuggtypen. |
| Shadow12 | 12 | Tolfte skuggtyp. |
| Shadow13 | 13 | Trettonde skuggtyp. |
| Shadow14 | 14 | Fjortonde skuggtyp. |
| Shadow15 | 15 | Femtonde skuggtyp. |
| Shadow16 | 16 | Sextonde skuggtyp. |
| Shadow17 | 17 | Sjuttonde skuggtyp. |
| Shadow18 | 18 | Artonde skuggtyp. |
| Shadow19 | 19 | Nittonde skuggtyp. |
| Shadow2 | 2 | Andra skuggtyp. |
| Shadow20 | 20 | Tjugonde skuggtyp. |
| Shadow21 | 21 | Tjugoförsta skuggtyp. |
| Shadow22 | 22 | Tjugoandra skuggtyp. |
| Shadow23 | 23 | Tjugotredje skuggtyp. |
| Shadow24 | 24 | Tjugofjärde skuggtyp. |
| Shadow25 | 25 | Tjugofemte skuggtyp. |
| Shadow26 | 26 | Tjugosjätte skuggtyp. |
| Shadow27 | 27 | Tjugosjunde skuggtyp. |
| Shadow28 | 28 | Tjugoåttonde skuggtyp. |
| Shadow29 | 29 | Tjugonionde skuggtyp. |
| Shadow3 | 3 | Tredje skuggtyp. |
| Shadow30 | 30 | Trettionde skuggtyp. |
| Shadow31 | 31 | Trettioförsta skuggtyp. |
| Shadow32 | 32 | Trettiotvåa skuggtyp. |
| Shadow33 | 33 | Trettiotredje skuggtyp. |
| Shadow34 | 34 | Trettiofjärde skuggtyp. |
| Shadow35 | 35 | Trettiofemte skuggtyp. |
| Shadow36 | 36 | Trettiosexte skuggtyp. |
| Shadow37 | 37 | Trettiosjunde skuggtyp. |
| Shadow38 | 38 | Trettioåttonde skuggtyp. |
| Shadow39 | 39 | Trettionionde skuggtyp. |
| Shadow4 | 4 | Fjärde skuggtyp. |
| Shadow40 | 40 | Fyrtioende skuggtyp. |
| Shadow41 | 41 | Fyrtioförsta skuggtyp. |
| Shadow42 | 42 | Fyrtiotvåa skuggtyp. |
| Shadow43 | 43 | Fyrtiotredje skuggtyp. |
| Shadow5 | 5 | Femte skuggtyp. |
| Shadow6 | 6 | Sjätte skuggtyp. |
| Shadow7 | 7 | Sjunde skuggtyp. |
| Shadow8 | 8 | Åttonde skuggtyp. |
| Shadow9 | 9 | Nionde skuggtyp. |


## Exempel



Visar hur man arbetar med skuggformatering för formen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

if (shape->get_ShadowFormat()->get_Visible() && shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::Shadow2)
{
    shape->get_ShadowFormat()->set_Type(Aspose::Words::Drawing::ShadowType::Shadow7);
}

if (shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::ShadowMixed)
{
    shape->get_ShadowFormat()->Clear();
}
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
