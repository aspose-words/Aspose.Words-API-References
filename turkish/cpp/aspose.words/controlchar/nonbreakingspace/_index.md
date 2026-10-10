---
title: "Aspose::Words::ControlChar::NonBreakingSpace metodu"
linktitle: "NonBreakingSpace"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ControlChar::NonBreakingSpace metodu. Kesintisiz boşluk karakteri: \"\\x00a0\" C++'da."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/controlchar/nonbreakingspace/
---
## ControlChar::NonBreakingSpace method


Bölünemez boşluk karakteri: "\x00a0".

```cpp
static System::String & Aspose::Words::ControlChar::NonBreakingSpace()
```


## Örnekler



Bir belgeye çeşitli kontrol karakterleri eklemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Normal bir boşluk ekle.
builder->Write(System::String(u"Before space.") + Aspose::Words::ControlChar::SpaceChar + u"After space.");

// Kırılmayan boşluk (NBSP) ekle.
// Normal boşluktan farklı olarak, bu boşluk konumunda otomatik satır sonu olamaz.
builder->Write(System::String(u"Before space.") + Aspose::Words::ControlChar::NonBreakingSpace() + u"After space.");

// Sekme karakteri ekle.
builder->Write(System::String(u"Before tab.") + Aspose::Words::ControlChar::Tab() + u"After tab.");

// Satır sonu ekle.
builder->Write(System::String(u"Before line break.") + Aspose::Words::ControlChar::LineBreak() + u"After line break.");

// Yeni bir satır ekle ve yeni bir paragraf başlat.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());
builder->Write(System::String(u"Before line feed.") + Aspose::Words::ControlChar::LineFeed() + u"After line feed.");
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());

// Satır besleme karakterinin iki sürümü vardır.
ASSERT_EQ(Aspose::Words::ControlChar::LineFeed(), Aspose::Words::ControlChar::Lf());

// Satır başı ve satır besleme tek bir karakterle birlikte temsil edilebilir.
ASSERT_EQ(Aspose::Words::ControlChar::CrLf(), Aspose::Words::ControlChar::Cr() + Aspose::Words::ControlChar::Lf());

// Paragraf sonu ekle, bu yeni bir paragraf başlatır.
builder->Write(System::String(u"Before paragraph break.") + Aspose::Words::ControlChar::ParagraphBreak() + u"After paragraph break.");
ASSERT_EQ(3, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());

// Bölüm sonu ekle. Bu yeni bir bölüm veya paragraf oluşturmaz.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
builder->Write(System::String(u"Before section break.") + Aspose::Words::ControlChar::SectionBreak() + u"After section break.");
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Sayfa sonu ekle.
builder->Write(System::String(u"Before page break.") + Aspose::Words::ControlChar::PageBreak() + u"After page break.");

// Sayfa sonu, bölüm sonu ile aynı değere sahiptir.
ASSERT_EQ(Aspose::Words::ControlChar::PageBreak(), Aspose::Words::ControlChar::SectionBreak());

// Yeni bir bölüm ekle ve ardından sütun sayısını ikiye ayarla.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc));
builder->MoveToSection(1);
builder->get_CurrentSection()->get_PageSetup()->get_TextColumns()->SetCount(2);

// Metnin bir sonraki sütuna geçtiği noktayı işaretlemek için bir kontrol karakteri kullanabiliriz.
builder->Write(System::String(u"Text at end of column 1.") + Aspose::Words::ControlChar::ColumnBreak() + u"Text at beginning of column 2.");

doc->Save(get_ArtifactsDir() + u"ControlChar.InsertControlChars.docx");

// Çoğu karakter için char ve string karşılıkları vardır.
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::Cell()), Aspose::Words::ControlChar::CellChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::NonBreakingSpace()), Aspose::Words::ControlChar::NonBreakingSpaceChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::Tab()), Aspose::Words::ControlChar::TabChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::LineBreak()), Aspose::Words::ControlChar::LineBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::LineFeed()), Aspose::Words::ControlChar::LineFeedChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::ParagraphBreak()), Aspose::Words::ControlChar::ParagraphBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::SectionBreak()), Aspose::Words::ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::PageBreak()), Aspose::Words::ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::ColumnBreak()), Aspose::Words::ControlChar::ColumnBreakChar);
```

## Ayrıca Bakınız

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
