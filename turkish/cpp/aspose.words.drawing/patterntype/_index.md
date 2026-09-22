---
title: "Aspose::Words::Drawing::PatternType enum"
linktitle: "PatternType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::PatternType enum. C++'ta bir şekli doldurmak için kullanılacak doldurma desenini belirtir."
type: docs
weight: 31000
url: /tr/cpp/aspose.words.drawing/patterntype/
---
## PatternType enum


Bir şekli doldurmak için kullanılacak doldurma desenini belirtir.

```cpp
enum class PatternType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | -1 | Desen yok. |
| Percent10 | 1 | Ön plan renginin %10'u. |
| Percent20 | 2 | Ön plan renginin %20'si. |
| Percent25 | 3 | Ön plan renginin %25'i. |
| Percent30 | 4 | Ön plan renginin %30'u. |
| Percent40 | 5 | Ön plan renginin %40'ı |
| Percent50 | 6 | Ön plan renginin %50'si |
| Percent5 | 7 | Ön plan renginin %5'i. |
| Percent60 | 8 | Ön plan renginin %60'ı. |
| Percent70 | 9 | Ön plan renginin %70'i. |
| Percent75 | 10 | Ön plan renginin %75'i. |
| Percent80 | 11 | Ön plan renginin %80'i. |
| Percent90 | 12 | Ön plan renginin %90'i. |
| Çapraz | 13 | Çapraz. |
| KoyuAşağıÇapraz | 14 | Koyu aşağı çapraz. |
| KoyuYatay | 15 | Koyu yatay. |
| KoyuYukarıÇapraz | 16 | Koyu yukarı çapraz. |
| KoyuDikey | 17 | Koyu dikey. |
| KesikliAşağıÇapraz | 18 | Kesikli aşağı çapraz. |
| KesikliYatay | 19 | Kesikli yatay. |
| KesikliYukarıÇapraz | 20 | Kesikli yukarı çapraz. |
| KesikliDikey | 21 | Kesikli dikey. |
| ÇaprazTuğla | 22 | Çapraz tuğla. |
| ÇaprazÇapraz | 23 | Çapraz çapraz. |
| Çukurluk | 24 | Desen çukurluk. |
| NoktalıElmas | 25 | Noktalı elmas. |
| NoktalıIzgara | 26 | Noktalı ızgara. |
| AşağıYönlüÇapraz | 27 | Aşağı yönlü çapraz. |
| Yatay | 28 | Yatay. |
| YatayTuğla | 29 | Yatay tuğla. |
| BüyükDamaTahtası | 30 | Büyük dama tahtası. |
| BüyükKonfeti | 31 | Büyük konfeti. |
| BüyükIzgara | 32 | Büyük ızgara. |
| AçıkAşağıYönlüÇapraz | 33 | Açık aşağı yönlü çapraz. |
| AçıkYatay | 34 | Açık yatay. |
| AçıkYukarıYönlüÇapraz | 36 | Açık yukarı yönlü çapraz. |
| AçıkDikey | 37 | Açık dikey. |
| DarYatay | 38 | Dar yatay. |
| DarDikey | 39 | Dar dikey. |
| ÇerçeveliElmas | 40 | Çerçeveli elmas. |
| Kareli | 41 | Kareli. |
| Kiremit | 42 | Kiremit. |
| KüçükDamalıTahta | 43 | Küçük damalı tahta. |
| KüçükKonfeti | 44 | Küçük konfeti. |
| KüçükIzgara | 45 | Küçük ızgara. |
| KatıElmas | 46 | Katı elmas. |
| Küre | 47 | Küre. |
| Kafes | 48 | Kafes. |
| YukarıÇapraz | 49 | Yukarı çapraz. |
| Dikey | 50 | Dikey. |
| Wave | 51 | Dalga. |
| Örme | 52 | Örme. |
| GenişAşağıÇapraz | 53 | Geniş aşağı çapraz. |
| WideUpwardDiagonal | 54 | Geniş yukarı diyagonal. |
| ZigZag | 55 | Zikzak. |


## Örnekler



Bir şekil için deseni nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Desene doldurmayı belirtmenin birkaç yolu vardır.
// 1 -  Deseni şekil doldurmasına uygula:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Ön plan ve arka plan renkleriyle deseni şekil doldurmasına uygula:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
