---
title: "Aspose::Words::Drawing::ShadowType enum"
linktitle: "ShadowType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShadowType enum. C++'da bir şekil gölgesinin türünü belirtir."
type: docs
weight: 35000
url: /tr/cpp/aspose.words.drawing/shadowtype/
---
## ShadowType enum


Bir şekil gölgesinin tipini belirtir.

```cpp
enum class ShadowType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| ShadowMixed | -2 | Önceden tanımlanmış gölge ön ayarlarından hiçbiri. |
| Shadow1 | 1 | İlk gölge türü. |
| Shadow10 | 10 | Onuncu gölge türü. |
| Shadow11 | 11 | On birinci gölge türü. |
| Shadow12 | 12 | On ikinci gölge türü. |
| Shadow13 | 13 | On üçüncü gölge türü. |
| Shadow14 | 14 | On dördüncü gölge türü. |
| Shadow15 | 15 | On beşinci gölge türü. |
| Shadow16 | 16 | On altıncı gölge türü. |
| Shadow17 | 17 | On yedinci gölge türü. |
| Shadow18 | 18 | On sekizinci gölge türü. |
| Shadow19 | 19 | On dokuzuncu gölge türü. |
| Shadow2 | 2 | İkinci gölge türü. |
| Shadow20 | 20 | Yirminci gölge türü. |
| Shadow21 | 21 | Yirmi birinci gölge türü. |
| Shadow22 | 22 | Yirmi ikinci gölge türü. |
| Shadow23 | 23 | Yirmi üçüncü gölge türü. |
| Shadow24 | 24 | Yirmi dördüncü gölge türü. |
| Shadow25 | 25 | Yirmi beşinci gölge türü. |
| Shadow26 | 26 | Yirmi altıncı gölge türü. |
| Shadow27 | 27 | Yirmi yedinci gölge türü. |
| Shadow28 | 28 | Yirmi sekizinci gölge türü. |
| Shadow29 | 29 | Yirmi dokuzuncu gölge türü. |
| Shadow3 | 3 | Üçüncü gölge türü. |
| Shadow30 | 30 | Otuzuncu gölge türü. |
| Shadow31 | 31 | Otuz birinci gölge türü. |
| Shadow32 | 32 | Otuz ikinci gölge türü. |
| Shadow33 | 33 | Otuz üçüncü gölge türü. |
| Shadow34 | 34 | Otuz dördüncü gölge türü. |
| Shadow35 | 35 | Otuz beşinci gölge türü. |
| Shadow36 | 36 | Otuz altıncı gölge türü. |
| Shadow37 | 37 | Otuz yedinci gölge türü. |
| Shadow38 | 38 | Otuz sekizinci gölge türü. |
| Shadow39 | 39 | Otuz dokuzuncu gölge türü. |
| Shadow4 | 4 | Dördüncü gölge türü. |
| Shadow40 | 40 | Kırkıncı gölge türü. |
| Shadow41 | 41 | Kırk birinci gölge türü. |
| Shadow42 | 42 | Kırk ikinci gölge türü. |
| Shadow43 | 43 | Kırk üçüncü gölge türü. |
| Shadow5 | 5 | Beşinci gölge türü. |
| Shadow6 | 6 | Altıncı gölge türü. |
| Shadow7 | 7 | Yedinci gölge türü. |
| Shadow8 | 8 | Sekizinci gölge türü. |
| Shadow9 | 9 | Dokuzuncu gölge türü. |


## Örnekler



Bir şekil için gölge biçimlendirmesiyle nasıl çalışılacağını gösterir.
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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
