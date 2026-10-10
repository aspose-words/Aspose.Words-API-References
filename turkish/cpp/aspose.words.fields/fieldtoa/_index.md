---
title: "Aspose::Words::Fields::FieldToa class"
linktitle: "FieldToa"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldToa sınıfı. TOA alanını uygular. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 104000
url: /tr/cpp/aspose.words.fields/fieldtoa/
---
## FieldToa class


TOA alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldToa : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Tabloyu oluşturmak için kullanılan belgenin bölümünü işaretleyen yer iminin adını alır. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_EntryCategory](./get_entrycategory/)() | Tabloya dahil edilen girişler için bütünsel kategoriyi alır. |
| [get_EntrySeparator](./get_entryseparator/)() | Yetkiler tablosu girişini ve sayfa numarasını ayırmak için kullanılan karakter dizisini alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Sayfa numarası listesinde iki sayfa numarasını ayırmak için kullanılan karakter dizisini alır. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Sayfa aralığının başlangıç ve bitişini ayırmak için kullanılan karakter dizisini alır. |
| [get_RemoveEntryFormatting](./get_removeentryformatting/)() | Belgedeki giriş metninin biçimlendirmesinin yetkiler tablosundaki girişten kaldırılıp kaldırılmayacağını alır. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_SequenceName](./get_sequencename/)() | Sayfa numarasıyla birlikte numarası eklenen bir dizinin adını alır. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Dizi numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter dizisini alır. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [get_UseHeading](./get_useheading/)() | Yetkiler tablosundaki girişler için kategori başlığının dahil edilip edilmeyeceğini alır. |
| [get_UsePassim](./get_usepassim/)() | Aynı yetkiye beş veya daha fazla farklı sayfa referansını, alıntılanan eserde bir kelime ya da pasajın sıkça geçtiğini göstermek için kullanılan "passim" ile değiştirip değiştirmeyeceğini alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Tabloyu oluşturmak için kullanılan belgenin bölümünü işaretleyen yer iminin adını ayarlar. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | Tabloya dahil edilen girişler için bütünsel kategoriyi ayarlar. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Yetkiler tablosu girişini ve sayfa numarasını ayırmak için kullanılan karakter dizisini ayarlar. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Sayfa numarası listesinde iki sayfa numarasını ayırmak için kullanılan karakter dizisini ayarlar. |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Sayfa aralığının başlangıç ve bitişini ayırmak için kullanılan karakter dizisini ayarlar. |
| [set_RemoveEntryFormatting](./set_removeentryformatting/)(bool) | Belgedeki giriş metninin biçimlendirmesinin yetkiler tablosundaki girişten kaldırılıp kaldırılmayacağını ayarlar. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Sayfa numarasıyla birlikte numarası eklenen bir dizinin adını ayarlar. |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Dizi numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter dizisini ayarlar. |
| [set_UseHeading](./set_useheading/)(bool) | Yetkiler tablosundaki girişler için kategori başlığının dahil edilip edilmeyeceğini ayarlar. |
| [set_UsePassim](./set_usepassim/)(bool) | Aynı kaynağa beş veya daha fazla farklı sayfa referansını "passim" ile değiştirip değiştirmeyeceği ayarlanır; "passim", alıntılanan eserde bir kelime ya da pasajın sık sık geçtiğini göstermek için kullanılır. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
