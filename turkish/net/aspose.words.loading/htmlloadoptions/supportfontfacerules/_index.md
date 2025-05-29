---
title: HtmlLoadOptions.SupportFontFaceRules
linktitle: SupportFontFaceRules
articleTitle: SupportFontFaceRules
second_title: .NET için Aspose.Words
description: HtmlLoadOptions SupportFontFaceRules'ı keşfedin, yazı tipi yüklemesini kolaylıkla kontrol edin. Cilalı bir görünüm için özel yazı tiplerini etkinleştirerek web tasarımınızı geliştirin.
type: docs
weight: 60
url: /tr/net/aspose.words.loading/htmlloadoptions/supportfontfacerules/
---
## HtmlLoadOptions.SupportFontFaceRules property

@font-face kurallarının desteklenip desteklenmeyeceğini ve beyan edilen fontların yüklenip yüklenmeyeceğini belirten bir değer alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool SupportFontFaceRules { get; set; }
```

## Notlar

Bu seçenek etkinleştirilirse, @font-face kurallarında bildirilen yazı tipleri yüklenir ve ortaya çıkan belgenin yazı tipi tanımlarına gömülür (bkz.[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) ). Bu, yüklenen yazı tiplerini işleme için kullanılabilir hale getirir ancak , kaydederken yazı tiplerinin gömülmesini otomatik olarak etkinleştirmez. Yüklenen yazı tipleriyle belgeyi kaydetmek için, [`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) mülkiyeti[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) koleksiyonu şu şekilde ayarlanmalıdır:`doğru` .

Desteklenen yazı tipi biçimleri TTF, EOT ve WOFF'dur.

@font-face kuralları SVG görüntüleri yüklenirken desteklenmiyor.

## Örnekler

Belirtilen "@font-face" kurallarının nasıl yükleneceğini gösterir.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();
loadOptions.SupportFontFaceRules = true;
Document doc = new Document(MyDir + "Html with FontFace.html", loadOptions);

Assert.AreEqual("Squarish Sans CT Regular", doc.FontInfos[0].Name);
```

### Ayrıca bakınız

* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
