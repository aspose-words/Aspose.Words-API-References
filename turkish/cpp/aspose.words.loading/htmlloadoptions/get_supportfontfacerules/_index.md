---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules metodu"
linktitle: "get_SupportFontFaceRules"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules metodu. @font-face kurallarını destekleyip desteklemeyeceğini ve bildirilen yazı tiplerini yükleyip yüklemeyeceğini belirten bir değeri alır veya ayarlar. Varsayılan değer C++'de false."
type: docs
weight: 6500
url: /tr/cpp/aspose.words.loading/htmlloadoptions/get_supportfontfacerules/
---
## HtmlLoadOptions::get_SupportFontFaceRules method


@font-face kurallarını destekleyip desteklemeyeceğini ve bildirilen yazı tiplerinin yüklenip yüklenmeyeceğini belirten bir değeri alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules() const
```

## Açıklamalar


Bu seçenek etkinleştirildiğinde, @font-face kurallarında bildirilen yazı tipleri yüklenir ve ortaya çıkan belgenin yazı tipi tanımlarına gömülür (bkz. [FontInfos](../../../aspose.words/documentbase/get_fontinfos/)). Bu, yüklü yazı tiplerinin render için kullanılabilir olmasını sağlar ancak kaydederken yazı tiplerinin otomatik olarak gömülmesini etkinleştirmez. Belgeyi yüklü yazı tipleriyle kaydetmek için, [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) özelliği [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) koleksiyonunda **true** olarak ayarlanmalıdır.

Desteklenen yazı tipi formatları TTF, EOT ve WOFF'tur.

@font-face kuralları SVG görüntüleri yüklenirken desteklenmez.

## Örnekler



Bildirilen "@font-face" kurallarının nasıl yükleneceğini gösterir.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_SupportFontFaceRules(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Html with FontFace.html", loadOptions);

ASSERT_EQ(u"Squarish Sans CT Regular", doc->get_FontInfos()->idx_get(0)->get_Name());
```

## Ayrıca Bakınız

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
