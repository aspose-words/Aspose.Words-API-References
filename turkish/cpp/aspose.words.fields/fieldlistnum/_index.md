---
title: "Aspose::Words::Fields::FieldListNum sınıfı"
linktitle: "FieldListNum"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldListNum sınıfı. LISTNUM alanını uygular. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 64000
url: /tr/cpp/aspose.words.fields/fieldlistnum/
---
## FieldListNum class


LISTNUM alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldListNum : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_HasListName](./get_haslistname/)() | Alan kodu tarafından bir soyut numaralandırma tanımının adının sağlanıp sağlanmadığını gösteren bir değer döndürür. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_ListLevel](./get_listlevel/)() | Alanının varsayılan davranışını geçersiz kılarak listedeki seviyeyi alır veya ayarlar. |
| [get_ListName](./get_listname/)() | Numaralandırma için kullanılan soyut numaralandırma tanımının adını alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_StartingNumber](./get_startingnumber/)() | Bu alan için başlangıç değerini alır veya ayarlar. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() override | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_ListLevel](./set_listlevel/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Fields::FieldListNum::get_ListLevel](./get_listlevel/). |
| [set_ListName](./set_listname/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Fields::FieldListNum::get_ListName](./get_listname/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_StartingNumber](./set_startingnumber/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Fields::FieldListNum::get_StartingNumber](./get_startingnumber/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

## Örnekler



LISTNUM alanlarıyla paragrafları numaralandırmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// LISTNUM alanları, her LISTNUM alanında artan bir sayı gösterir.
// Bu alanların ayrıca numaralı listeleri taklit etmemizi sağlayan çeşitli seçenekleri vardır.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// Listeler varsayılan olarak 1'den saymaya başlar, ancak bu sayıyı 0 gibi farklı bir değere ayarlayabiliriz.
// Bu alan "0)" görüntüler.
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// LISTNUM alanları her liste seviyesi için ayrı sayımlar tutar.
// Başka bir LISTNUM alanı ile aynı paragrafta bir LISTNUM alanı eklemek
// sayım yerine liste seviyesini artırır.
// Sonraki alan, yukarıda başlattığımız sayımı devam ettirecek ve liste seviyesi 1'de "1" değerini gösterecektir.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Bu alan, liste seviyesi 2'de bir sayım başlatacak. "1" değerini gösterecektir.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Bu alan, liste seviyesi 3'de bir sayım başlatacak. "1" değerini gösterecektir.
// Farklı liste seviyelerinin farklı biçimlendirmeleri vardır,
// bu yüzden bu alanlar birleştirildiğinde "1)a)i)" değerini gösterir.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// Eklediğimiz bir sonraki LISTNUM alanı, liste seviyesinde sayımı devam ettirecek
// önceki LISTNUM alanının bulunduğu seviyede.
// "ListLevel" özelliğini kullanarak farklı bir liste seviyesine atlayabiliriz.
// Bu LISTNUM alanı liste seviyesi 3'te kalırsa, "ii)" gösterirdi,
// ancak, onu liste seviyesi 2'ye taşıdığımız için, o seviyede sayımı sürdürür ve "b)" gösterir.
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// Alanı farklı bir AUTONUM alan türünü taklit ettirmek için ListName özelliğini ayarlayabiliriz.
// "NumberDefault" AUTONUM'u, "OutlineDefault" AUTONUMOUT'u taklit eder,
// ve "LegalDefault" AUTONUMLGL alanlarını taklit eder.
// "OutlineDefault" liste adı, başlangıç numarası 1 olduğunda "I." görüntülenir.
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// ListName önceki alandan devralınmaz, bu yüzden her yeni alan için ayarlamamız gerekir.
// Bu alan, farklı liste adıyla sayımı devam ettirir ve "II." görüntüler.
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
