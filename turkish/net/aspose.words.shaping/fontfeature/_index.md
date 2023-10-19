---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: Aspose.Words for .NET
description: Aspose.Words.Shaping.FontFeature Sıralama. Özellikler bir komut dosyasını oluşturmak için bir yazı tipinde gliflerin nasıl kullanıldığı hakkında bilgi sağlar. https//docs.microsoft.com/enus/typography/opentype/spec/featuretags C#'da.
type: docs
weight: 6030
url: /tr/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

Özellikler, bir komut dosyasını oluşturmak için bir yazı tipinde gliflerin nasıl kullanıldığı hakkında bilgi sağlar. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | Glif alternatiflerinin sayısını en aza indirmek için, bazen bir karakterin varsayılan glifini iki veya daha fazla glif halinde ayrıştırmak tercih edilebilir. Ayrıca, daha iyi bir glif için iki veya daha fazla karakter için varsayılan gliflerin tek bir glif halinde oluşturulması tercih edilebilir. işleme. Bu özellik bu tür birleştirmeye/ayrışmaya izin verir. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp Eşdeğer OpenType etiketi: 'ccmp' |
| StandardLigatures | `1818847073` | Bir glif dizisini, tipografik amaçlar için tercih edilen tek bir glifle değiştirir. Bu özellik, tasarımcının/üreticinin normal koşullarda kullanılması gerektiğine karar verdiği bitişik harfleri kapsar. Eşdeğer OpenType etiketi: 'liga' https://docs .microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | Tipografik amaçlar için tercih edilen bir glif dizisini tek bir glifle değiştirir. Bu özellik, komut dosyasının normal koşullarda kullanılması gerektiğini belirlediği bitişik harfleri kapsar. Bu özellik, bazı komut dosyaları için doğru glif oluşumunu sağlamak açısından önemlidir. . https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig Eşdeğer OpenType etiketi: 'rlig' |
| ContextualLigatures | `1668049255` | Bir glif dizisini tipografik amaçlar için tercih edilen tek bir glifle değiştirir. Diğer bitişik harf özelliklerinden farklı olarak, 'clig' bitişik harfin önerildiği bağlamı belirtir. Bu yetenek bazı komut dosyası tasarımlarında ve eğik bitişik harfler için önemlidir. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig Eşdeğer OpenType etiketi: 'clig' |
| DiscretionaryLigatures | `1684826471` | Bir glif dizisini tipografik amaçlarla tercih edilen tek bir glifle değiştirir. Bu özellik, kullanıcının tercihine göre özel efekt için kullanılabilecek bitişik harfleri kapsar. https://docs.microsoft.com/en-us /typography/opentype/spec/features_ae#dlig Eşdeğer OpenType etiketi: 'dlig' |
| HistoricalLigatures | `1751935335` | Bazı bitişik harfler geçmişte yaygın olarak kullanılıyordu, ancak bugün anakronik görünmektedir. Bazı yazı tipleri, alternatif olarak tarihsel formları içerir, dolayısıyla bir "nokta" efekti için kullanılabilirler. Bu özellik, varsayılan (geçerli) formların yerine, tarihsel alternatifler. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig Eşdeğer OpenType etiketi: 'hlig' |
| ProportionalFigures | `1886287213` | Tek tip (tablo) genişliklere ayarlanmış şekil gliflerini, gliflere özgü (orantılı) genişliklere ayarlanmış karşılık gelen gliflerle değiştirir. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum Eşdeğer OpenType etiketi: 'pnum' |
| TabularFigures | `1953396077` | Orantılı genişliklerde ayarlanan şekil gliflerini, tekdüze (tablo) genişliklerde ayarlanmış karşılık gelen gliflerle değiştirir. Tablo genişlikleri genellikle varsayılan olacaktır, ancak bu güvenli bir şekilde varsayılamaz. Elbette bu özellik tek aralıklı tasarımlarda mevcut olmayacaktır. https ://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum Eşdeğer OpenType etiketi: 'tnum' |
| LiningFigures | `1819178349` | Bu özellik, seçilen astarsız şekilleri astarlı şekillere dönüştürür. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum Eşdeğer OpenType etiketi: 'lnum' |
| OldstyleFigures | `1869509997` | Bu özellik, seçilen şekilleri varsayılan veya astar stilinden eski stil forma değiştirir. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum Eşdeğer OpenType etiketi: 'onum' |
| VerticalAlternates | `1986359924` | Varsayılan glifleri dikey yazma modunda dik sunuma uygun gliflere dönüştürür. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert Eşdeğer OpenType etiketi: 'vert' |
| VerticalAlternatesAndRotation | `1987212338` | Bazı sabit genişlikli (yarım, üçüncü veya çeyrek genişlik) veya orantılı genişlikteki glifleri (çoğunlukla Latince veya katakana) dikey yazmaya uygun formlarla (yani saat yönünde 90 derece döndürülmüş) değiştirir. https:// docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 Eşdeğer OpenType etiketi: 'vrt2' |
| StylisticSet01 | `1936928817` | Biçimsel Küme 1 Bireysel gliflerin biçimsel alternatiflerine ek olarak veya bunların yerine (bkz. 'tuz' özelliği), bazı yazı tipleri, karakter kümesinin bölümlerine karşılık gelen biçimsel değişken glif kümeleri içerebilir, örneğin küçük harfler için birden fazla değişken Latin yazı tipi. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 Eşdeğer OpenType etiketi: 'ss01' |
| StylisticSet02 | `1936928818` | Biçimsel Küme 2 Eşdeğer OpenType etiketi: 'ss02' |
| StylisticSet03 | `1936928819` | Biçimsel Küme 3 Eşdeğer OpenType etiketi: 'ss03' |
| StylisticSet04 | `1936928820` | Biçimsel Küme 4 Eşdeğer OpenType etiketi: 'ss04' |
| StylisticSet05 | `1936928821` | Biçimsel Küme 5 Eşdeğer OpenType etiketi: 'ss05' |
| StylisticSet06 | `1936928822` | Biçimsel Küme 6 Eşdeğer OpenType etiketi: 'ss06' |
| StylisticSet07 | `1936928823` | Biçimsel Küme 7 Eşdeğer OpenType etiketi: 'ss07' |
| StylisticSet08 | `1936928824` | Biçimsel Küme 8 Eşdeğer OpenType etiketi: 'ss08' |
| StylisticSet09 | `1936928825` | Biçimsel Küme 9 Eşdeğer OpenType etiketi: 'ss09' |
| StylisticSet10 | `1936929072` | Biçimsel Küme 10 Eşdeğer OpenType etiketi: 'ss10' |
| StylisticSet11 | `1936929073` | Biçimsel Küme 11 Eşdeğer OpenType etiketi: 'ss11' |
| StylisticSet12 | `1936929074` | Biçimsel Küme 12 Eşdeğer OpenType etiketi: 'ss12' |
| StylisticSet13 | `1936929075` | Biçimsel Küme 13 Eşdeğer OpenType etiketi: 'ss13' |
| StylisticSet14 | `1936929076` | Biçimsel Küme 14 Eşdeğer OpenType etiketi: 'ss14' |
| StylisticSet15 | `1936929077` | Biçimsel Küme 15 Eşdeğer OpenType etiketi: 'ss15' |
| StylisticSet16 | `1936929078` | Biçimsel Küme 16 Eşdeğer OpenType etiketi: 'ss16' |
| StylisticSet17 | `1936929079` | Biçimsel Küme 17 Eşdeğer OpenType etiketi: 'ss17' |
| StylisticSet18 | `1936929080` | Biçimsel Küme 18 Eşdeğer OpenType etiketi: 'ss18' |
| StylisticSet19 | `1936929081` | Biçimsel Küme 19 Eşdeğer OpenType etiketi: 'ss19' |
| StylisticSet20 | `1936929328` | Biçimsel Küme 20 Eşdeğer OpenType etiketi: 'ss20' |
| Kerning | `1801810542` | Genellikle glifler arasında optik olarak tutarlı boşluk sağlamak için glifler arasındaki boşluk miktarını ayarlar. İyi tasarlanmış bir yazı tipi genel olarak tutarlı glifler arası boşluğa sahip olsa da, bazı glif kombinasyonları daha iyi okunabilirlik için ayarlama gerektirir. Yatay yönde standart ayarlamanın yanı sıra, bu özellik, aygıt tabloları aracılığıyla boyuta bağlı karakter aralığı verilerini, Y metin yönünde "çapraz akış" karakter aralığını ve gelişmiş ayardan bağımsız olarak glif yerleşiminin ayarlanmasını sağlayabilir. Bu özelliğin ikiden fazla çalıştırma için geçerli olabileceğini unutmayın gliflerdir ve tek aralıklı yazı tiplerinde kullanılmaz. Ayrıca bu özelliğin dikey olarak ayarlanmış metinler için geçerli olmadığını unutmayın. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern Eşdeğer OpenType etiketi: 'kern' |

### Ayrıca bakınız

* ad alanı [Aspose.Words.Shaping](../../aspose.words.shaping/)
* toplantı [Aspose.Words](../../)
