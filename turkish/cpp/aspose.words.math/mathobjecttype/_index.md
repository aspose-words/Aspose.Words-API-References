---
title: "Aspose::Words::Math::MathObjectType enum"
linktitle: "MathObjectType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Math::MathObjectType enum. C++'da bir Office Math nesnesinin türünü belirtir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.math/mathobjecttype/
---
## MathObjectType enum


Office [Math](../) nesnesinin türünü belirtir.

```cpp
enum class MathObjectType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| OMath | 0 | Matematiksel metnin bir örneği. |
| OMathPara | 1 | [Math](../) paragrafı veya görüntüleme matematik bölgesi, görüntüleme modundaki bir veya daha fazla [OMath](./) öğesi içerir. |
| Accent | 2 | Bir temel ve birleştirici diakritik işaretten oluşan Accent işlevi. |
| Bar | 3 | Bir temel argüman ve üst çizgi veya alt çizgi içeren Bar işlevi. |
| BorderBox | 4 | [Border](../../aspose.words/border/) Box nesnesi, matematiksel metnin (örneğin bir formül veya denklem) bir örneği etrafına çizilen bir kenarlık içeren. |
| Box | 5 | Bir denklem ya da diğer matematiksel metin örneklerinin bileşenlerini gruplamak için kullanılan Box nesnesi. |
| Ayırıcı | 6 | Ayırıcı nesnesi, açma ve kapama ayırıcılarından (parantez, süslü parantez, köşeli parantez ve dikey çubuk gibi) oluşur ve içinde bir öğe bulunur. |
| Derece | 7 | Matematiksel kökteki derece. |
| Argument | 8 | Argüman nesnesi. Office [Math](../) varlıklarını, diğer Office [Math](../) varlıklarına argüman olarak kullanıldıklarında kapsar. |
| Dizi | 9 | Dizi nesnesi, bir veya daha fazla denklem, ifade veya diğer matematiksel metin akışlarından oluşur ve satırdaki çevre metne göre dikey olarak bir birim olarak hizalanabilir. |
| Kesir | 10 | Kesir nesnesi, bir kesir çubuğu ile ayrılmış pay ve paydadan oluşur. |
| Payda | 11 | Bir kesir nesnesinin paydası. |
| Pay | 12 | Kesir nesnesinin payı. |
| Fonksiyon | 13 | Fonksiyon-Uygulama nesnesi, bir fonksiyon adı ve üzerine uygulanacak bir argüman öğesinden oluşur. |
| FonksiyonAdı | 14 | Fonksiyonun adı. Örneğin, fonksiyon adları sin ve cos'tur. |
| GrupKarakteri | 15 | Grup-Karakter nesnesi, metnin üstüne veya altına çizilen bir karakterden oluşur ve genellikle öğeleri görsel olarak gruplamak amacıyla kullanılır. |
| Limit | 16 | [LowerLimit](./) nesnesinin alt sınırı ve [UpperLimit](./) fonksiyonunun üst sınırı. |
| AltSınır | 17 | Alt-Sınır nesnesi, temel çizgi üzerindeki metin ve hemen altında daha küçük boyutta metinden oluşur. |
| ÜstSınır | 18 | Üst-Sınır nesnesi, temel çizgi üzerindeki metin ve hemen üstünde daha küçük boyutta metinden oluşur. |
| Matris | 19 | Matris nesnesi, bir veya daha fazla satır ve bir veya daha fazla sütunda düzenlenmiş bir veya daha fazla öğeden oluşur. |
| MatrixRow | 20 | Matrisin tek satırı. |
| NAry | 21 | n-ary nesne, bir n-ary nesne, bir temel (veya operand) ve isteğe bağlı üst ve alt limitlerden oluşur. |
| Phantom | 22 | Hayalet nesne. |
| Radical | 23 | Kök nesne, bir kök, bir temel öğe ve isteğe bağlı bir derece içerir. |
| SubscriptPart | 24 | Alt simge, alt simge kısmına sahip olabilen nesnenin alt simgesidir. |
| SuperscriptPart | 25 | Üst simge, üst simge nesnesinin üst simgesidir. |
| PreSubSuperscript | 26 | Ön-Alt-Üst Simge nesnesi, bir temel öğe ile temelin sol tarafına yerleştirilmiş bir alt ve bir üst simgeden oluşur. |
| Subscript | 27 | Alt simge nesnesi, bir temel öğe ve sağ altına yerleştirilmiş küçültülmüş bir alt simgeden oluşur. |
| SubSuperscript | 28 | Alt-üst simge nesnesi, bir temel öğe, sağ altına yerleştirilmiş küçültülmüş bir alt simge ve sağ üstüne yerleştirilmiş küçültülmüş bir üst simgeden oluşur. |
| Superscript | 29 | Üst simge nesnesi, bir temel öğe ve sağ üstüne yerleştirilmiş küçültülmüş bir üst simgeden oluşur. |
| None | 30 | Nesne türü belirtilmemiştir. |

## Ayrıca Bakınız

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
