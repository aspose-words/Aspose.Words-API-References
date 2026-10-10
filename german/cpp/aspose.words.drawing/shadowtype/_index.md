---
title: "Aspose::Words::Drawing::ShadowType enum"
linktitle: "ShadowType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShadowType enum. Gibt den Typ eines Formschattens in C++ an."
type: docs
weight: 35000
url: /de/cpp/aspose.words.drawing/shadowtype/
---
## ShadowType enum


Gibt den Typ eines Formschattens an.

```cpp
enum class ShadowType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| ShadowMixed | -2 | Keiner der vordefinierten Schatten-Voreinstellungen. |
| Shadow1 | 1 | Erster Schatten-Typ. |
| Shadow10 | 10 | Zehnter Schatten-Typ. |
| Shadow11 | 11 | Elfter Schattentyp. |
| Shadow12 | 12 | Zwölfter Schattentyp. |
| Shadow13 | 13 | Dreizehnter Schattentyp. |
| Shadow14 | 14 | Vierzehnter Schattentyp. |
| Shadow15 | 15 | Fünfzehnter Schattentyp. |
| Shadow16 | 16 | Sechzehnter Schattentyp. |
| Shadow17 | 17 | Siebzehnter Schattentyp. |
| Shadow18 | 18 | Achtzehnter Schattentyp. |
| Shadow19 | 19 | Neunzehnter Schattentyp. |
| Shadow2 | 2 | Zweiter Schattentyp. |
| Shadow20 | 20 | Zwanzigster Schattentyp. |
| Shadow21 | 21 | Einundzwanzigster Schattentyp. |
| Shadow22 | 22 | Zweiundzwanzigster Schattentyp. |
| Shadow23 | 23 | Dreiundzwanzigster Schatten-Typ. |
| Shadow24 | 24 | Vierundzwanzigster Schatten-Typ. |
| Shadow25 | 25 | Fünfundzwanzigster Schatten-Typ. |
| Shadow26 | 26 | Sechsundzwanzigster Schatten-Typ. |
| Shadow27 | 27 | Siebenundzwanzigster Schatten-Typ. |
| Shadow28 | 28 | Achtundzwanzigster Schatten-Typ. |
| Shadow29 | 29 | Neunundzwanzigster Schatten-Typ. |
| Shadow3 | 3 | Dritter Schatten-Typ. |
| Shadow30 | 30 | Dreißigster Schatten-Typ. |
| Shadow31 | 31 | Einunddreißigster Schatten-Typ. |
| Shadow32 | 32 | Zweiunddreißigster Schatten-Typ. |
| Shadow33 | 33 | Dreiunddreißigster Schatten-Typ. |
| Shadow34 | 34 | Dreißig vierte Schattenart. |
| Shadow35 | 35 | Dreißig fünfte Schattenart. |
| Shadow36 | 36 | Dreißig sechste Schattenart. |
| Shadow37 | 37 | Dreißig siebte Schattenart. |
| Shadow38 | 38 | Dreißig achte Schattenart. |
| Shadow39 | 39 | Dreißig neunte Schattenart. |
| Shadow4 | 4 | Vierte Schattenart. |
| Shadow40 | 40 | Vierzigste Schattenart. |
| Shadow41 | 41 | Einundvierzigste Schattenart. |
| Shadow42 | 42 | Zweiundvierzigste Schattenart. |
| Shadow43 | 43 | Dreiundvierzigste Schattenart. |
| Shadow5 | 5 | Fünfte Schattenart. |
| Shadow6 | 6 | Sechste Schattenart. |
| Shadow7 | 7 | Siebter Schattentyp. |
| Shadow8 | 8 | Achter Schattentyp. |
| Shadow9 | 9 | Neunter Schattentyp. |


## Beispiele



Zeigt, wie man mit einer Schattenformatierung für die Form arbeitet.
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

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
