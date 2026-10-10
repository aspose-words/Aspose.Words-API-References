---
title: "Aspose::Words::Fields::FieldMergeField class"
linktitle: "FieldMergeField"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldMergeField class. MERGEFIELD alanını uygular. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 67000
url: /tr/cpp/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class


MERGEFIELD alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldMergeField : public Aspose::Words::Fields::Field,
                        public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldName](./get_fieldname/)() | Bir veri alanının adını alır. |
| [get_FieldNameNoPrefix](./get_fieldnamenoprefix/)() const | Sadece veri alanının adını döndürür. Herhangi bir önek, prefix özelliğine göre kaldırılır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_IsMapped](./get_ismapped/)() | Bu alanın eşlenmiş bir alan olup olmadığını alır. |
| [get_IsVerticalFormatting](./get_isverticalformatting/)() | Dikey biçimlendirme için karakter dönüşümünün etkinleştirilip etkinleştirilmeyeceğini alır. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_TextAfter](./get_textafter/)() | Alan boş değilse, alandan sonra eklenecek metni alır. |
| [get_TextBefore](./get_textbefore/)() | Alan boş değilse, alandan önce eklenecek metni alır. |
| [get_Type](./get_type/)() const override | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_FieldName](./set_fieldname/)(const System::String\&) | Bir veri alanının adını ayarlar. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_IsMapped](./set_ismapped/)(bool) | Bu alanın eşlenmiş bir alan olup olmadığını ayarlar. |
| [set_IsVerticalFormatting](./set_isverticalformatting/)(bool) | Dikey biçimlendirme için karakter dönüşümünün etkinleştirilip etkinleştirilmeyeceğini ayarlar. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_TextAfter](./set_textafter/)(const System::String\&) | Alan boş değilse, alandan sonra eklenecek metni ayarlar. |
| [set_TextBefore](./set_textbefore/)(const System::String\&) | Alan boş değilse, alandan önce eklenecek metni ayarlar. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
