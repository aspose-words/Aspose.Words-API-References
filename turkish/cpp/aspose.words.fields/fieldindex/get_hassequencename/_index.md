---
title: "Aspose::Words::Fields::FieldIndex::get_HasSequenceName metodu"
linktitle: "get_HasSequenceName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIndex::get_HasSequenceName metodu. C++'da alanın sonucunun oluşturulması sırasında bir dizinin kullanılıp kullanılmayacağını gösteren bir değer alır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.fields/fieldindex/get_hassequencename/
---
## FieldIndex::get_HasSequenceName method


Alan sonucunun oluşturulması sırasında bir dizinin kullanılıp kullanılmayacağını gösteren bir değeri alır.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_HasSequenceName()
```


## Örnekler



INDEX ve SEQ alanlarını birleştirerek bir belgeyi parçalara nasıl bölüneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgedeki her XE alanı için bir giriş gösteren bir INDEX alanı oluşturun.
// Her giriş, XE alanının Text özelliği değerini sol tarafta gösterir,
// ve XE alanını içeren sayfanın numarasını sağ tarafta.
// Eğer XE alanlarının "Text" özelliğindeki değer aynı ise,
// INDEX alanı onları tek bir girişte gruplayacak.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// SequenceName özelliğinde bir SEQ alanı dizisi adlandırın. Bu INDEX alanının her girişi artık şunu da gösterecek
// bu girişi oluşturan XE alanı konumunda dizinin sayımının bulunduğu sayı.
index->set_SequenceName(u"MySequence");

// Kullanıcıya anlamlarını açıklamak için dizi ve sayfa numaralarının etrafında yer alacak metni ayarlayın.
// Bu yapılandırma ile oluşturulan bir giriş, sayfa numarasına "MySequence at 1 on page 1" gibi bir şey gösterecektir.
// PageNumberSeparator ve SequenceSeparator 15 karakterden uzun olamaz.
index->set_PageNumberSeparator(u"\tMySequence at ");
index->set_SequenceSeparator(u" on page ");
ASSERT_TRUE(index->get_HasSequenceName());

ASSERT_EQ(u" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index->GetFieldCode());

// SEQ alanları, her SEQ alanında artan bir sayım gösterir.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımlar tutar.
// SEQ alanının "SequenceIdentifier" özelliğiyle tanımlanır.
// "MySequence" dizisini 1'e taşıyan bir SEQ alanı ekleyin.
// Bu alan normal belge metninden farklı değildir. Bir INDEX alanının içindekiler tablosunda görünmez.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", sequenceField->GetFieldCode());

// INDEX alanında bir giriş oluşturacak bir XE alanı ekleyin.
// "MySequence" 1'de olduğu ve bu XE alanı 2. sayfada olduğu için, yukarıda tanımladığımız özel ayırıcılarla birlikte,
// bu alanın INDEX girişi sol tarafta "Cat" ve sağ tarafta "MySequence at 1 on page 2" görüntülenecek.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

ASSERT_EQ(u" XE  Cat", indexEntry->GetFieldCode());

// Bir sayfa sonu ekleyin ve SEQ alanlarını kullanarak "MySequence" değerini 3'e ilerletin.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

// Yukarıdakiyle aynı Text özelliğine sahip bir XE alanı ekleyin.
// INDEX girişi, "Text" özelliğinde eşleşen değerlere sahip XE alanlarını gruplayacak
// her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişte birleştirir.
// Sayfa 2'de "MySequence" 3 olduğundan, ", 3 on page 3" aynı INDEX girdisine yukarıda olduğu gibi eklenecek.
// Bu INDEX girdisinin sayfa numarası bölümü artık "MySequence at 1 on page 2, 3 on page 3" gösterecek.
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

// Yeni ve benzersiz bir Text özelliği değeriyle bir XE alanı ekleyin.
// Bu, sayfa 4'te MySequence 3 olan yeni bir giriş ekleyecek.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Dog");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Sequence.docx");
```

## Ayrıca Bakınız

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
