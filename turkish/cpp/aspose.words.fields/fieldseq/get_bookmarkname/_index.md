---
title: "Aspose::Words::Fields::FieldSeq::get_BookmarkName metodu"
linktitle: "get_BookmarkName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldSeq::get_BookmarkName metodu. C++'ta belge içinde mevcut konum yerine başka bir yerdeki öğeye referans veren bir yer imi adını alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldseq/get_bookmarkname/
---
## FieldSeq::get_BookmarkName method


Belgenin mevcut konumunda değil, başka bir yerdeki bir öğeye referans veren bir yer imi adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_BookmarkName()
```


## Örnekler



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

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
