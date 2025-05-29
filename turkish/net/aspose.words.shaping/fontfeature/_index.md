---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: .NET için Aspose.Words
description: Aspose.Words.Shaping.FontFeature enum'unu keşfedin, yazı tiplerinde betik oluşturma için glif kullanımını ayrıntılı olarak açıklayın. Tipografi bilginizi bugün geliştirin!
type: docs
weight: 6860
url: /tr/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

Özellikler, bir yazı tipinde betiğin oluşturulması için gliflerin nasıl kullanıldığı hakkında bilgi sağlar. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | Glif alternatiflerinin sayısını en aza indirmek için, bazen bir karakterin varsayılan glifini iki veya daha fazla glife ayırmak istenebilir. Ek olarak, daha iyi glif işleme için iki veya daha fazla karakterin varsayılan gliflerini tek bir glife ayırmak tercih edilebilir. Bu özellik, bu tür bir kompozisyon/ayrıştırmaya izin verir. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp Eşdeğer OpenType etiketi: 'ccmp' |
| StandardLigatures | `1818847073` | Tipografik amaçlar için tercih edilen tek bir glifle bir dizi glifi değiştirir. Bu özellik, tasarımcının/üreticinin normal koşullarda kullanılması gerektiğine karar verdiği bağları kapsar. Eşdeğer OpenType etiketi: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | Tipografik amaçlar için tercih edilen tek bir glifle bir glif dizisini değiştirir. Bu özellik, betiğin normal koşullarda kullanılması gerektiğini belirlediği bağları kapsar. Bu özellik, bazı betikler için doğru glif oluşumunu sağlamak açısından önemlidir. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig Eşdeğer OpenType etiketi: 'rlig' |
| ContextualLigatures | `1668049255` | Tipografik amaçlar için tercih edilen tek bir glifle bir dizi glifi değiştirir. Diğer bağlama özelliklerinin aksine, 'clig', bağlamanın önerildiği bağlamı belirtir. Bu yetenek bazı betik tasarımlarında ve eğik bağlamalar için önemlidir. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig Eşdeğer OpenType etiketi: 'clig' |
| DiscretionaryLigatures | `1684826471` | Tipografik amaçlar için tercih edilen tek bir glifle bir dizi glifi değiştirir. Bu özellik, kullanıcının tercihine göre özel efekt için kullanılabilecek bağları kapsar. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#dlig Eşdeğer OpenType etiketi: 'dlig' |
| HistoricalLigatures | `1751935335` | Bazı bağlar geçmişte yaygın olarak kullanılıyordu, ancak bugün anakronistik görünüyor. Bazı yazı tipleri, alternatif olarak tarihi formları içerir, böylece bir "dönem" efekti için kullanılabilirler. Bu özellik varsayılan (geçerli) formları tarihi alternatiflerle değiştirir. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig Eşdeğer OpenType etiketi: 'hlig' |
| ProportionalFigures | `1886287213` | Tekdüze (tablo) genişliklerde ayarlanan şekil gliflerini, glif-özel (orantılı) genişliklerde ayarlanan karşılık gelen gliflerle değiştirir. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum Eşdeğer OpenType etiketi: 'pnum' |
| TabularFigures | `1953396077` | Orantılı genişliklere ayarlanmış şekil gliflerini, tekdüze (tablo) genişliklere ayarlanmış karşılık gelen gliflerle değiştirir. Tablo genişlikleri genellikle varsayılan olacaktır, ancak bu güvenli bir şekilde varsayılamaz. Elbette bu özellik sabit aralıklı tasarımlarda mevcut olmayacaktır. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum Eşdeğer OpenType etiketi: 'tnum' |
| LiningFigures | `1819178349` | Bu özellik seçili çizgi olmayan şekilleri çizgi şekillerine dönüştürür. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum Eşdeğer OpenType etiketi: 'lnum' |
| OldstyleFigures | `1869509997` | Bu özellik seçili şekilleri varsayılan veya çizgi stilinden eski stile değiştirir. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum Eşdeğer OpenType etiketi: 'onum' |
| VerticalAlternates | `1986359924` | Varsayılan glifleri, dikey yazma modunda dik sunum için uygun gliflere dönüştürür. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert Eşdeğer OpenType etiketi: 'vert' |
| VerticalAlternatesAndRotation | `1987212338` | Bazı sabit genişlikli (yarım, üçte bir veya çeyrek genişlikli) veya orantılı genişlikteki glifleri (çoğunlukla Latin veya katakana) dikey yazmaya uygun biçimlerle (yani saat yönünde 90 derece döndürülmüş) değiştirir. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 Eşdeğer OpenType etiketi: 'vrt2' |
| StylisticSet01 | `1936928817` | Stilistik Set 1 Bireysel gliflerin stilistik alternatiflerine ek olarak veya bunların yerine (bkz. 'salt' özelliği), bazı yazı tipleri karakter setinin bölümlerine karşılık gelen stilistik varyant glifleri kümeleri içerebilir, örneğin Latin yazı tipindeki küçük harfler için birden fazla varyant. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 Eşdeğer OpenType etiketi: 'ss01' |
| StylisticSet02 | `1936928818` | Stilistik Set 2 Eşdeğer OpenType etiketi: 'ss02' |
| StylisticSet03 | `1936928819` | Stilistik Set 3 Eşdeğer OpenType etiketi: 'ss03' |
| StylisticSet04 | `1936928820` | Stilistik Set 4 Eşdeğer OpenType etiketi: 'ss04' |
| StylisticSet05 | `1936928821` | Stilistik Set 5 Eşdeğer OpenType etiketi: 'ss05' |
| StylisticSet06 | `1936928822` | Stilistik Set 6 Eşdeğer OpenType etiketi: 'ss06' |
| StylisticSet07 | `1936928823` | Stilistik Set 7 Eşdeğer OpenType etiketi: 'ss07' |
| StylisticSet08 | `1936928824` | Stilistik Set 8 Eşdeğer OpenType etiketi: 'ss08' |
| StylisticSet09 | `1936928825` | Stilistik Set 9 Eşdeğer OpenType etiketi: 'ss09' |
| StylisticSet10 | `1936929072` | Stilistik Set 10 Eşdeğer OpenType etiketi: 'ss10' |
| StylisticSet11 | `1936929073` | Stilistik Set 11 Eşdeğer OpenType etiketi: 'ss11' |
| StylisticSet12 | `1936929074` | Stilistik Set 12 Eşdeğer OpenType etiketi: 'ss12' |
| StylisticSet13 | `1936929075` | Stilistik Set 13 Eşdeğer OpenType etiketi: 'ss13' |
| StylisticSet14 | `1936929076` | Stilistik Set 14 Eşdeğer OpenType etiketi: 'ss14' |
| StylisticSet15 | `1936929077` | Stilistik Set 15 Eşdeğer OpenType etiketi: 'ss15' |
| StylisticSet16 | `1936929078` | Stilistik Set 16 Eşdeğer OpenType etiketi: 'ss16' |
| StylisticSet17 | `1936929079` | Stilistik Set 17 Eşdeğer OpenType etiketi: 'ss17' |
| StylisticSet18 | `1936929080` | Stilistik Set 18 Eşdeğer OpenType etiketi: 'ss18' |
| StylisticSet19 | `1936929081` | Stilistik Set 19 Eşdeğer OpenType etiketi: 'ss19' |
| StylisticSet20 | `1936929328` | Stilistik Set 20 Eşdeğer OpenType etiketi: 'ss20' |
| Kerning | `1801810542` | Genellikle glifler arasında optik olarak tutarlı aralık sağlamak için glifler arasındaki boşluk miktarını ayarlar. İyi tasarlanmış bir yazı tipi genel olarak tutarlı glifler arası aralığa sahip olsa da, bazı glif birleşimlerinin daha iyi okunabilirlik için ayarlanması gerekir. Yatay yöndeki standart ayarlamanın yanı sıra, bu özellik cihaz tabloları aracılığıyla boyuta bağlı harf aralığı verisi, Y metin yönünde "çapraz akış" harf aralığı ve gelişmiş ayarlamadan bağımsız olarak glif yerleşiminin ayarlanması sağlayabilir. Bu özelliğin iki gliften fazlasına uygulanabileceğini ve sabit aralıklı yazı tiplerinde kullanılmayacağını unutmayın. Ayrıca, bu özelliğin dikey olarak ayarlanmış metinlere uygulanmadığını unutmayın. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern Eşdeğer OpenType etiketi: 'çekirdek' |

### Ayrıca bakınız

* ad alanı [Aspose.Words.Shaping](../../aspose.words.shaping/)
* toplantı [Aspose.Words](../../)
