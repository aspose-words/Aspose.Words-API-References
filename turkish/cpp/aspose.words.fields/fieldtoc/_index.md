---
title: "Aspose::Words::Fields::FieldToc sınıfı"
linktitle: "FieldToc"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldToc sınıfı. TOC alanını uygular. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 105000
url: /tr/cpp/aspose.words.fields/fieldtoc/
---
## FieldToc class


TOC alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldToc : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [FieldToc](./fieldtoc/)() |  |
| [get_BookmarkName](./get_bookmarkname/)() | Tabloyu oluşturmak için kullanılan belgenin bölümünü işaretleyen yer iminin adını alır. |
| [get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/)() | Şekil tablosu oluşturulurken başlığın etiketi ve numarası dahil edilmeyen sıralama tanımlayıcısının adını alır veya ayarlar. |
| [get_CustomStyles](./get_customstyles/)() | İçindekiler tablosuna dahil edilecek, yerleşik başlık stilleri dışındaki stillerin listesini alır. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_EntryIdentifier](./get_entryidentifier/)() | Dahil edilen TC alanlarının tip tanımlayıcılarıyla eşleşmesi gereken bir dizeyi alır. |
| [get_EntryLevelRange](./get_entrylevelrange/)() | İçindekiler tablosu girişlerinin dahil edilecek seviye aralığını alır. |
| [get_EntrySeparator](./get_entryseparator/)() | Bir giriş ile sayfa numarasını ayıran karakter dizisini alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_HeadingLevelRange](./get_headinglevelrange/)() | Dahil edilecek başlık seviyelerinin aralığını alır. |
| [get_HideInWebLayout](./get_hideinweblayout/)() | Web düzen görünümünde sekme lideri ve sayfa numaralarının gizlenip gizlenmeyeceğini alır. |
| [get_InsertHyperlinks](./get_inserthyperlinks/)() | İçindekiler tablosu girişlerini hiperlink yapıp yapmayacağını alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/)() | İçindekiler tablosu girişlerinin sayfa numaralarının atlanacağı seviye aralığını alır. |
| [get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/)() | Girişin sayfa numarasına bir önek eklenmesi gereken sıralamanın tanımlayıcısını alır veya ayarlar. |
| [get_PreserveLineBreaks](./get_preservelinebreaks/)() | Tablo girişleri içinde yeni satır karakterlerinin korunup korunmayacağını alır. |
| [get_PreserveTabs](./get_preservetabs/)() | Tablo girişleri içinde sekme girişlerinin korunup korunmayacağını alır. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Dizi numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_TableOfFiguresLabel](./get_tableoffigureslabel/)() | Şekil tablosu oluşturulurken kullanılan sıralama tanımlayıcısının adını alır veya ayarlar. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/)() | Uygulanan paragraf taslak seviyesinin kullanılıp kullanılmayacağını alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Tabloyu oluşturmak için kullanılan belgenin bölümünü işaretleyen yer iminin adını ayarlar. |
| [set_CaptionlessTableOfFiguresLabel](./set_captionlesstableoffigureslabel/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/). |
| [set_CustomStyles](./set_customstyles/)(const System::String\&) | İçindekiler tablosuna dahil edilecek, yerleşik başlık stilleri dışındaki stillerin listesini ayarlar. |
| [set_EntryIdentifier](./set_entryidentifier/)(const System::String\&) | Dahil edilen TC alanlarının tip tanımlayıcılarıyla eşleşmesi gereken bir dizeyi ayarlar. |
| [set_EntryLevelRange](./set_entrylevelrange/)(const System::String\&) | İçindekiler tablosu girişlerinin dahil edilecek seviye aralığını ayarlar. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Bir giriş ile sayfa numarasını ayıran karakter dizisini ayarlar. |
| [set_HeadingLevelRange](./set_headinglevelrange/)(const System::String\&) | Dahil edilecek başlık seviyelerinin aralığını ayarlar. |
| [set_HideInWebLayout](./set_hideinweblayout/)(bool) | Web düzen görünümünde sekme lideri ve sayfa numaralarının gizlenip gizlenmeyeceğini ayarlar. |
| [set_InsertHyperlinks](./set_inserthyperlinks/)(bool) | İçindekiler tablosu girişlerini hiperlink yapıp yapmayacağını ayarlar. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_PageNumberOmittingLevelRange](./set_pagenumberomittinglevelrange/)(const System::String\&) | İçindekiler tablosu girişlerinin sayfa numaralarının atlanacağı seviyeler aralığını ayarlar. |
| [set_PrefixedSequenceIdentifier](./set_prefixedsequenceidentifier/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/). |
| [set_PreserveLineBreaks](./set_preservelinebreaks/)(bool) | Tablo girişleri içinde yeni satır karakterlerinin korunup korunmayacağını ayarlar. |
| [set_PreserveTabs](./set_preservetabs/)(bool) | Tablo girişleri içinde sekme karakterlerinin korunup korunmayacağını ayarlar. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldToc::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_TableOfFiguresLabel](./set_tableoffigureslabel/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel](./get_tableoffigureslabel/). |
| [set_UseParagraphOutlineLevel](./set_useparagraphoutlinelevel/)(bool) | Uygulanan paragraf taslak seviyesinin kullanılıp kullanılmayacağını ayarlar. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [UpdatePageNumbers](./updatepagenumbers/)() | Bu içindekiler tablosundaki öğeler için sayfa numaralarını günceller. |

## Örnekler



SEQ alanlarını kullanarak bir TOC alanını girdilerle nasıl dolduracağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir TOC alanı, belgede bulunan her SEQ alanı için içindekiler tablosunda bir giriş oluşturabilir.
// Her giriş, SEQ alanını içeren paragrafı ve alanın göründüğü sayfa numarasını içerir.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// SEQ alanları, her SEQ alanında artan bir sayım gösterir.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımlar tutar.
// SEQ alanının "SequenceIdentifier" özelliğiyle tanımlanır.
// "TableOfFiguresLabel" özelliğini kullanarak TOC için bir ana sıra adlandırın.
// Artık bu TOC, "SequenceIdentifier" özelliği "MySequence" olarak ayarlanmış SEQ alanlarından yalnızca girişler oluşturacaktır.
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// "PrefixedSequenceIdentifier" özelliğinde başka bir SEQ alanı sırasını adlandırabiliriz.
// Bu önek sırasındaki SEQ alanları TOC girişleri oluşturmayacaktır.
// Ana sıra SEQ alanından oluşturulan her TOC girişi artık şu sayacı da gösterecek ki
// girişi oluşturan birincil sıra SEQ alanında önek sırasının şu anda bulunduğu sayıyı.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// Her TOC girişi, önek sıra sayacını hemen solunda gösterecektir
// ana sıra SEQ alanının göründüğü sayfa numarasının.
// Bu iki sayı arasında görünecek özel bir ayırıcı belirtebiliriz.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Bu TOC'yi doldurmak için SEQ alanlarını kullanmanın iki yolu vardır.
// 1 -  TOC'nin önek sırasına ait bir SEQ alanı eklemek:
// Bu alan, "PrefixSequence" için SEQ sıra sayacını 1 artıracaktır.
// Bu alan, tanımlanan ana sıraya ait olmadığından
// "TableOfFiguresLabel" özelliğiyle TOC'de tanımlanan, bir giriş olarak görünmeyecektir.
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 -  TOC'nin ana sırasına ait bir SEQ alanı eklemek:
// Bu SEQ alanı TOC'de bir giriş oluşturacaktır.
// TOC girişi, SEQ alanının bulunduğu paragrafı ve göründüğü sayfa numarasını içerecektir.
// Bu giriş ayrıca önek sırasının şu anda bulunduğu sayacı da gösterecek,
// sayfa numarasından, TOC'nin SeqenceSeparator özelliğindeki değerle ayrılmış olarak.
// "PrefixSequence" sayacı 1'de, bu ana sıra SEQ alanı sayfa 2'de,
// ve ayırıcı ">" olduğundan, giriş "1>2" olarak gösterilecektir.
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Bir sayfa ekleyin, önek sırasını 2 artırın ve ardından bir SEQ alanı ekleyerek TOC girişi oluşturun.
// Önek sırası artık 2'de, ve ana sıra SEQ alanı sayfa 3'te,
// bu yüzden TOC girişi sayfa sayısında "2>3" olarak gösterilecektir.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
