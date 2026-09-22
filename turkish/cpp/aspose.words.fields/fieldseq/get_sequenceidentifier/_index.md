---
title: "Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier metodu"
linktitle: "get_SequenceIdentifier"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier metodu. C++'ta numaralandırılacak öğe serisine atanan adı alır veya ayarlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.fields/fieldseq/get_sequenceidentifier/
---
## FieldSeq::get_SequenceIdentifier method


Numaralanacak öğe serisine atanan adı alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier()
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

## Ayrıca Bakınız

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
