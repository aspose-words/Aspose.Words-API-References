---
title: "Aspose::Words::Fields::FieldCitation sınıfı"
linktitle: "FieldCitation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldCitation sınıfı. CITATION alanını uygular. Daha fazla bilgi edinmek için C++'daki belgelendirme makalesini ziyaret edin."
type: docs
weight: 22000
url: /tr/cpp/aspose.words.fields/fieldcitation/
---
## FieldCitation class


CITATION alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldCitation : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AnotherSourceTag](./get_anothersourcetag/)() | Alıntıya dahil edilecek başka bir kaynağın **Tag** öğesinin değerine eşleşen bir değeri alır. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | Belgedeki alıntıyı biçimlendirmek için belirtilen bibliyografik stil ile birlikte kullanılan dil kimliğini alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_PageNumber](./get_pagenumber/)() | Alıntıyla ilişkili bir sayfa numarasını alır. |
| [get_Prefix](./get_prefix/)() | Alıntının önüne eklenen bir ön eki alır. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_SourceTag](./get_sourcetag/)() | Eklenecek kaynağın **Tag** öğesinin değerine eşleşen bir değeri alır. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Suffix](./get_suffix/)() | Alıntının sonuna eklenen bir soneki alır. |
| [get_SuppressAuthor](./get_suppressauthor/)() | Alıntıdan yazar bilgisinin gizlenip gizlenmediğini alır. |
| [get_SuppressTitle](./get_suppresstitle/)() | Alıntıdan başlık bilgisinin gizlenip gizlenmediğini alır. |
| [get_SuppressYear](./get_suppressyear/)() | Alıntıdan yıl bilgisinin gizlenip gizlenmediğini alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [get_VolumeNumber](./get_volumenumber/)() | Alıntıyla ilişkili bir cilt numarasını alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_AnotherSourceTag](./set_anothersourcetag/)(const System::String\&) | Alıntıya dahil edilecek başka bir kaynağın **Tag** öğesinin değerine eşleşen bir değeri ayarlar. |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | Belgedeki alıntıyı biçimlendirmek için belirtilen bibliyografik stil ile birlikte kullanılan dil kimliğini ayarlar. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_PageNumber](./set_pagenumber/)(const System::String\&) | Alıntıyla ilişkili bir sayfa numarasını ayarlar. |
| [set_Prefix](./set_prefix/)(const System::String\&) | Alıntının önüne eklenen bir ön eki ayarlar. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | Eklenecek kaynağın **Tag** öğesinin değerine eşleşen bir değeri ayarlar. |
| [set_Suffix](./set_suffix/)(const System::String\&) | Alıntının sonuna eklenen bir soneki ayarlar. |
| [set_SuppressAuthor](./set_suppressauthor/)(bool) | Alıntıdan yazar bilgisinin gizlenip gizlenmeyeceğini ayarlar. |
| [set_SuppressTitle](./set_suppresstitle/)(bool) | Alıntıdan başlık bilgisinin gizlenip gizlenmeyeceğini ayarlar. |
| [set_SuppressYear](./set_suppressyear/)(bool) | Alıntıdan yıl bilgisinin gizlenip gizlenmeyeceğini ayarlar. |
| [set_VolumeNumber](./set_volumenumber/)(const System::String\&) | Alıntıyla ilişkili bir cilt numarasını ayarlar. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
