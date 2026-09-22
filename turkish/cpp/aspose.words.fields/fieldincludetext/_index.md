---
title: "Aspose::Words::Fields::FieldIncludeText sınıfı"
linktitle: "FieldIncludeText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIncludeText sınıfı. INCLUDETEXT alanını uygular. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 58000
url: /tr/cpp/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class


INCLUDETEXT alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldIncludeText : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                         public Aspose::Words::Fields::IFieldIncludeTextCode
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | Dahil edilecek belgede yer iminin adını alır. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_Encoding](./get_encoding/)() | Referans alınan dosya içindeki veriye uygulanan kodlamayı alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_LockFields](./get_lockfields/)() override | Dahil edilen belgede alanların güncellenmesini önleyip önlemeyeceğini alır. |
| [get_MimeType](./get_mimetype/)() | Referans alınan dosyanın MIME tipini alır. |
| [get_NamespaceMappings](./get_namespacemappings/)() override | XPath sorguları için ad alanı eşlemelerini alır. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_SourceFullName](./get_sourcefullname/)() override | Bir IRI kullanarak belgenin konumunu alır. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_TextConverter](./get_textconverter/)() override | Dahil edilen dosyanın formatı için metin dönüştürücünün adını alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [get_XPath](./get_xpath/)() override | XML dosyasının istenen bölümü için XPath'i alır. |
| [get_XslTransformation](./get_xsltransformation/)() override | XML verisini biçimlendirmek için XSL Dönüşümünün konumunu alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Dahil edilecek belgede yer iminin adını ayarlar. |
| [set_Encoding](./set_encoding/)(const System::String\&) | Referans alınan dosya içindeki veriye uygulanan kodlamayı ayarlar. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_LockFields](./set_lockfields/)(bool) | Dahil edilen belgede alanların güncellenmesini önleyip önlemeyeceğini ayarlar. |
| [set_MimeType](./set_mimetype/)(const System::String\&) | Referans alınan dosyanın MIME tipini ayarlar. |
| [set_NamespaceMappings](./set_namespacemappings/)(const System::String\&) | XPath sorguları için ad alanı eşlemelerini ayarlar. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Bir IRI kullanarak belgenin konumunu ayarlar. |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | Ekli dosyanın formatı için metin dönüştürücünün adını ayarlar. |
| [set_XPath](./set_xpath/)(const System::String\&) | XML dosyasının istenen bölümü için XPath'i ayarlar. |
| [set_XslTransformation](./set_xsltransformation/)(const System::String\&) | XML verisini biçimlendirmek için XSL Dönüşümünün konumunu ayarlar. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
