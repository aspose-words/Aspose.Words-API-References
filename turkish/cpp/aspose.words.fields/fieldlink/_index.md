---
title: "Aspose::Words::Fields::FieldLink sınıfı"
linktitle: "FieldLink"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldLink sınıfı. LINK alanını uygular. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 63000
url: /tr/cpp/aspose.words.fields/fieldlink/
---
## FieldLink class


LINK alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldLink : public Aspose::Words::Fields::Field,
                  public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | Bu alanın otomatik olarak güncellenip güncellenmeyeceğini alır. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_FormatUpdateType](./get_formatupdatetype/)() | Bağlı nesnenin biçimlendirmesini nasıl güncellediğini alır. |
| [get_InsertAsBitmap](./get_insertasbitmap/)() | Bağlantılı nesnenin bitmap olarak eklenip eklenmeyeceğini alır. |
| [get_InsertAsHtml](./get_insertashtml/)() | Bağlantılı nesnenin HTML biçiminde metin olarak eklenip eklenmeyeceğini alır. |
| [get_InsertAsPicture](./get_insertaspicture/)() | Bağlantılı nesnenin resim olarak eklenip eklenmeyeceğini alır. |
| [get_InsertAsRtf](./get_insertasrtf/)() | Bağlantılı nesnenin zengin metin biçiminde (RTF) eklenip eklenmeyeceğini alır. |
| [get_InsertAsText](./get_insertastext/)() | Bağlantılı nesnenin yalnızca metin biçiminde eklenip eklenmeyeceğini alır. |
| [get_InsertAsUnicode](./get_insertasunicode/)() | Bağlantılı nesnenin Unicode metin olarak eklenip eklenmeyeceğini alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLinked](./get_islinked/)() | Grafik verilerini belgeyle birlikte saklamayarak dosya boyutunu küçültüp küçültmeyeceğini alır. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_ProgId](./get_progid/)() | Bağlantı bilgisinin uygulama türünü alır. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_SourceFullName](./get_sourcefullname/)() | Kaynak dosyanın adını ve konumunu alır. |
| [get_SourceItem](./get_sourceitem/)() | Bağlantı verilen kaynak dosyanın bölümünü alır. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_AutoUpdate](./set_autoupdate/)(bool) | Bu alanın otomatik olarak güncellenip güncellenmeyeceğini ayarlar. |
| [set_FormatUpdateType](./set_formatupdatetype/)(const System::String\&) | Bağlı nesnenin biçimlendirmesini nasıl güncellediğini ayarlar. |
| [set_InsertAsBitmap](./set_insertasbitmap/)(bool) | Bağlantılı nesnenin bitmap olarak eklenip eklenmeyeceğini ayarlar. |
| [set_InsertAsHtml](./set_insertashtml/)(bool) | Bağlantılı nesnenin HTML biçiminde metin olarak eklenip eklenmeyeceğini ayarlar. |
| [set_InsertAsPicture](./set_insertaspicture/)(bool) | Bağlantılı nesnenin resim olarak eklenip eklenmeyeceğini ayarlar. |
| [set_InsertAsRtf](./set_insertasrtf/)(bool) | Bağlantılı nesnenin zengin metin biçiminde (RTF) eklenip eklenmeyeceğini ayarlar. |
| [set_InsertAsText](./set_insertastext/)(bool) | Bağlantılı nesnenin yalnızca metin biçiminde eklenip eklenmeyeceğini ayarlar. |
| [set_InsertAsUnicode](./set_insertasunicode/)(bool) | Bağlı nesnenin Unicode metin olarak eklenip eklenmeyeceğini ayarlar. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLinked](./set_islinked/)(bool) | Belgeyle birlikte grafik verileri depolanmayarak dosya boyutunun küçültülüp küçültülmeyeceğini ayarlar. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_ProgId](./set_progid/)(const System::String\&) | Bağlantı bilgilerinin uygulama türünü ayarlar. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Kaynak dosyanın adını ve konumunu ayarlar. |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Bağlantı verilen kaynak dosyanın bölümünü ayarlar. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
