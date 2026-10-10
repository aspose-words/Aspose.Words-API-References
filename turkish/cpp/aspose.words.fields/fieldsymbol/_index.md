---
title: "Aspose::Words::Fields::FieldSymbol class"
linktitle: "FieldSymbol"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldSymbol sınıfı. Bir SYMBOL alanını uygular. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 98000
url: /tr/cpp/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class


SYMBOL alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldSymbol : public Aspose::Words::Fields::Field,
                    public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_CharacterCode](./get_charactercode/)() | Karakterin kod noktası değerini ondalık veya onaltılık olarak alır veya ayarlar. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_DontAffectsLineSpacing](./get_dontaffectslinespacing/)() | Alan tarafından alınan karakterin paragrafın satır aralığını etkileyip etkilemeyeceğini alır veya ayarlar. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_FontName](./get_fontname/)() | Alan tarafından alınan karakterin yazı tipinin adını alır veya ayarlar. |
| [get_FontSize](./get_fontsize/)() | Alan tarafından alınan karakterin yazı tipinin punto cinsinden boyutunu alır veya ayarlar. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsAnsi](./get_isansi/)() | Karakter kodunun bir ANSI karakter değeri olarak yorumlanıp yorumlanmayacağını alır veya ayarlar. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_IsShiftJis](./get_isshiftjis/)() | Karakter kodunun bir SHIFT-JIS karakter değeri olarak yorumlanıp yorumlanmayacağını alır veya ayarlar. |
| [get_IsUnicode](./get_isunicode/)() | Karakter kodunun bir Unicode karakter değeri olarak yorumlanıp yorumlanmayacağını alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_CharacterCode](./set_charactercode/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldSymbol::get_CharacterCode](./get_charactercode/). |
| [set_DontAffectsLineSpacing](./set_dontaffectslinespacing/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldSymbol::get_DontAffectsLineSpacing](./get_dontaffectslinespacing/). |
| [set_FontName](./set_fontname/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldSymbol::get_FontName](./get_fontname/). |
| [set_FontSize](./set_fontsize/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldSymbol::get_FontSize](./get_fontsize/). |
| [set_IsAnsi](./set_isansi/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldSymbol::get_IsAnsi](./get_isansi/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_IsShiftJis](./set_isshiftjis/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldSymbol::get_IsShiftJis](./get_isshiftjis/). |
| [set_IsUnicode](./set_isunicode/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldSymbol::get_IsUnicode](./get_isunicode/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

## Örnekler



SYMBOL alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda tek bir karakteri görüntülemek için bir SYMBOL alanını kullanmanın üç yolu verilmiştir.
// 1 -  ANSI karakter kodu ile belirtilen © (Telif Hakkı) sembolünü gösteren bir SYMBOL alanı ekleyin:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// ANSI karakter kodu "U+00A9" veya tamsayı biçiminde "169", telif hakkı sembolü için ayrılmıştır.
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 -  ∞ (Sonsuzluk) sembolünü gösteren bir SYMBOL alanı ekleyin ve görünümünü değiştirin:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// Unicode'da, sonsuzluk sembolü "221E" kodunu kaplar.
field->set_CharacterCode(System::Convert::ToString(0x221E));
field->set_IsUnicode(true);

// Windows Karakter Haritası'nı kullandıktan sonra sembolümüzün yazı tipini değiştirin.
// yazı tipinin bu sembolü temsil edebildiğinden emin olmak için.
field->set_FontName(u"Calibri");
field->set_FontSize(u"24");

// Uzun semboller için bu bayrağı ayarlayarak, satırdaki metnin geri kalanını aşağı itmelerini önleyebiliriz.
field->set_DontAffectsLineSpacing(true);

ASSERT_EQ(u" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field->GetFieldCode());

builder->Writeln(u"Line 2");

// 3 -  あ karakterini gösteren bir SYMBOL alanı ekleyin,
// Shift-JIS (Windows-932) kod sayfasını destekleyen bir yazı tipiyle:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
