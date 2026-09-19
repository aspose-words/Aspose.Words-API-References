---
title: "Enum Aspose::Words::Drawing::ShadowType"
linktitle: "ShadowType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::Drawing::ShadowType. Specifica il tipo di ombra di una forma in C++."
type: docs
weight: 35000
url: /it/cpp/aspose.words.drawing/shadowtype/
---
## ShadowType enum


Specifica il tipo di ombra di una forma.

```cpp
enum class ShadowType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| ShadowMixed | -2 | Nessuno dei preset di ombra predefiniti. |
| Shadow1 | 1 | Primo tipo di ombra. |
| Shadow10 | 10 | Decimo tipo di ombra. |
| Shadow11 | 11 | Undicesimo tipo di ombra. |
| Shadow12 | 12 | Dodicesimo tipo di ombra. |
| Shadow13 | 13 | Tredicesimo tipo di ombra. |
| Shadow14 | 14 | Quattordicesimo tipo di ombra. |
| Shadow15 | 15 | Quindicesimo tipo di ombra. |
| Shadow16 | 16 | Sedicesimo tipo di ombra. |
| Shadow17 | 17 | Diciassettesimo tipo di ombra. |
| Shadow18 | 18 | Diciottesimo tipo di ombra. |
| Shadow19 | 19 | Diciannovesimo tipo di ombra. |
| Shadow2 | 2 | Secondo tipo di ombra. |
| Shadow20 | 20 | Ventesimo tipo di ombra. |
| Shadow21 | 21 | Ventunesimo tipo di ombra. |
| Shadow22 | 22 | Ventiduesimo tipo di ombra. |
| Shadow23 | 23 | Ventitreesimo tipo di ombra. |
| Shadow24 | 24 | Ventiquattresimo tipo di ombra. |
| Shadow25 | 25 | Venticinquesimo tipo di ombra. |
| Shadow26 | 26 | Ventiseiesimo tipo di ombra. |
| Shadow27 | 27 | Ventisettesimo tipo di ombra. |
| Shadow28 | 28 | Ventottesimo tipo di ombra. |
| Shadow29 | 29 | Ventinovesimo tipo di ombra. |
| Shadow3 | 3 | Terzo tipo di ombra. |
| Shadow30 | 30 | Trentesimo tipo di ombra. |
| Shadow31 | 31 | Trentunesimo tipo di ombra. |
| Shadow32 | 32 | Trentaduesimo tipo di ombra. |
| Shadow33 | 33 | Trentunesimo tipo di ombra. |
| Shadow34 | 34 | Trentaquattresimo tipo di ombra. |
| Shadow35 | 35 | Trentacinquesimo tipo di ombra. |
| Shadow36 | 36 | Trentaseiesimo tipo di ombra. |
| Shadow37 | 37 | Trentasettesimo tipo di ombra. |
| Shadow38 | 38 | Trentottesimo tipo di ombra. |
| Shadow39 | 39 | Trentanovesimo tipo di ombra. |
| Shadow4 | 4 | Quarto tipo di ombra. |
| Shadow40 | 40 | Quarantesimo tipo di ombra. |
| Shadow41 | 41 | Quarantunesimo tipo di ombra. |
| Shadow42 | 42 | Quarantaduesimo tipo di ombra. |
| Shadow43 | 43 | Quarantatresimo tipo di ombra. |
| Shadow5 | 5 | Quinto tipo di ombra. |
| Shadow6 | 6 | Sesto tipo di ombra. |
| Shadow7 | 7 | Settimo tipo di ombra. |
| Shadow8 | 8 | Ottavo tipo di ombra. |
| Shadow9 | 9 | Nono tipo di ombra. |


## Esempi



Mostra come lavorare con la formattazione dell'ombra per la forma.
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

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
