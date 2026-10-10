---
title: "Aspose::Words::Fields::FieldSeq class"
linktitle: "FieldSeq"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldSeq sınıfı. SEQ alanını uygular. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 91000
url: /tr/cpp/aspose.words.fields/fieldseq/
---
## FieldSeq class


SEQ alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldSeq : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Belgenin mevcut konumunda değil, başka bir yerdeki bir öğeye referans veren bir yer imi adını alır veya ayarlar. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_InsertNextNumber](./get_insertnextnumber/)() | Belirtilen öğe için bir sonraki sıra numarasının eklenip eklenmeyeceğini alır veya ayarlar. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_ResetHeadingLevel](./get_resetheadinglevel/)() | Sıra numarasını sıfırlamak için bir başlık seviyesini temsil eden tam sayı değerini alır veya ayarlar. Sayı yoksa -1 döndürür. |
| [get_ResetNumber](./get_resetnumber/)() | Sıra numarasını sıfırlamak için tam sayı değerini alır veya ayarlar. Sayı yoksa -1 döndürür. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_SequenceIdentifier](./get_sequenceidentifier/)() | Numaralanacak öğe serisine atanan adı alır veya ayarlar. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | [Aspose::Words::Fields::FieldSeq::get_BookmarkName](./get_bookmarkname/) için ayarlayıcı. |
| [set_InsertNextNumber](./set_insertnextnumber/)(bool) | [Aspose::Words::Fields::FieldSeq::get_InsertNextNumber](./get_insertnextnumber/) için ayarlayıcı. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_ResetHeadingLevel](./set_resetheadinglevel/)(const System::String\&) | [Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel](./get_resetheadinglevel/) için ayarlayıcı. |
| [set_ResetNumber](./set_resetnumber/)(const System::String\&) | [Aspose::Words::Fields::FieldSeq::get_ResetNumber](./get_resetnumber/) için ayarlayıcı. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_SequenceIdentifier](./set_sequenceidentifier/)(const System::String\&) | [Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier](./get_sequenceidentifier/) için ayarlayıcı. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

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


SEQ alanlarını kullanarak numaralandırma oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// SEQ alanları, her SEQ alanında artan bir sayım gösterir.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımlar tutar.
// SEQ alanının "SequenceIdentifier" özelliğiyle tanımlanır.
// Mevcut sayım değerini "MySequence" olarak gösterecek bir SEQ alanı ekleyin,
// "ResetNumber" özelliğini kullanarak 100'e ayarladıktan sonra.
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// Bu dizideki bir sonraki sayıyı başka bir SEQ alanı ile gösterin.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// Seviye 1 başlık ekleyin.
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Aynı diziden başka bir SEQ alanı ekleyin ve sayımı her başlıkta 1'e sıfırlayacak şekilde yapılandırın.
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// Yukarıdaki başlık bir seviye 1 başlıktır, bu yüzden bu dizi için sayım 1'e sıfırlanır.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// Bu dizinin bir sonraki sayısına geçin.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```


İçindekiler tablosu ve dizi alanlarını nasıl birleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir TOC alanı, belgede bulunan her SEQ alanı için içindekiler tablosunda bir giriş oluşturabilir.
// Her giriş, SEQ alanını içeren paragrafı içerir,
// ve alanın göründüğü sayfanın numarasını.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Bu TOC alanını "MySequence" değerine sahip bir SequenceIdentifier özelliği olacak şekilde yapılandırın.
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Bu TOC alanını yalnızca bir yer işaretinin sınırları içinde olan SEQ alanlarını alacak şekilde yapılandırın
// "TOCBookmark" adlı.
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// SEQ alanları, her SEQ alanında artan bir sayım gösterir.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımlar tutar.
// SEQ alanının "SequenceIdentifier" özelliğiyle tanımlanır.
// TOC'un
// TableOfFiguresLabel özelliği. Bu alan, dışarıda olduğu için TOC'de bir giriş oluşturmayacaktır
// "BookmarkName" tarafından belirlenen yer işareti sınırları içinde.
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// Bu SEQ alanının dizisi, TOC'un "TableOfFiguresLabel" özelliğiyle eşleşir ve yer işareti sınırları içindedir.
// Bu alanı içeren paragraf, TOC'de bir giriş olarak görünecektir.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// Bu SEQ alanının dizisi, TOC'un "TableOfFiguresLabel" özelliğiyle eşleşmez,
// ve yer işareti sınırları içindedir. Paragrafı TOC'de bir giriş olarak görünmeyecektir.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// Bu SEQ alanının dizisi, TOC'un "TableOfFiguresLabel" özelliğiyle eşleşir ve yer işareti sınırları içindedir.
// Bu alan ayrıca başka bir yer işaretine referans verir. O yer işaretinin içeriği, bu SEQ alanı için TOC girişinde görünecektir.
// SEQ alanı kendisi o yer işaretinin içeriğini göstermeyecektir.
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// Yukarıdaki SEQ alanının ona referans vermesi nedeniyle, içeriği TOC girişinde görünecek bir yer işareti oluşturun.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
