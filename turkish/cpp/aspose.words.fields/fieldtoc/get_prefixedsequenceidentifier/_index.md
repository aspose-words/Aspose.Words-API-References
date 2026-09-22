---
title: "Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier yöntemi"
linktitle: "get_PrefixedSequenceIdentifier"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier yöntemi. C++'da bir girişin sayfa numarasına ön ek eklenmesi gereken dizinin tanımlayıcısını alır veya ayarlar."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.fields/fieldtoc/get_prefixedsequenceidentifier/
---
## FieldToc::get_PrefixedSequenceIdentifier method


Girişin sayfa numarasına bir önek eklenmesi gereken sıralamanın tanımlayıcısını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier()
```


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

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
