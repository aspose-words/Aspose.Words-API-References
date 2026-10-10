---
title: "Aspose::Words::Comparing::ComparisonTargetType enum"
linktitle: "ComparisonTargetType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comparing::ComparisonTargetType enum. Karşılaştırma sırasında kullanılacak temel belgeyi belirtmeye olanak tanır. Varsayılan değer C++'da Current'tır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.comparing/comparisontargettype/
---
## ComparisonTargetType enum


Karşılaştırma sırasında kullanılacak temel belgeyi belirtmeye olanak tanır. Varsayılan değer [Current](./)'dır.

```cpp
enum class ComparisonTargetType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Mevcut | 0 | Bu belge, karşılaştırma sırasında temel olarak kullanılır. |
| Yeni | 1 | Diğer belge, karşılaştırma sırasında temel olarak kullanılır. |


## Örnekler



Karşılaştırma yaparken belirli belge öğesi türlerini nasıl filtreleyeceğinizi gösterir.
```cpp
// Orijinal belgeyi oluşturun ve çeşitli öğelerle doldurun.
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);

// Dipnotla referans verilen paragraf metni:
builder->Writeln(u"Hello world! This is the first paragraph.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Original endnote text.");

// Tablo:
builder->StartTable();
builder->InsertCell();
builder->Write(u"Original cell 1 text");
builder->InsertCell();
builder->Write(u"Original cell 2 text");
builder->EndTable();

// Metin Kutusu:
System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 20);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"Original textbox contents");

// TARİH alanı:
builder->MoveTo(docOriginal->get_FirstSection()->get_Body()->AppendParagraph(u""));
builder->InsertField(u" DATE ");

// Yorum:
auto newComment = System::MakeObject<Aspose::Words::Comment>(docOriginal, u"John Doe", u"J.D.", System::DateTime::get_Now());
newComment->SetText(u"Original comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(newComment);

// Üstbilgi:
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Original header contents.");

// Belgemizin bir kopyasını oluşturun ve kopyalanmış belgenin her bir öğesinde hızlı bir düzenleme yapın.
auto docEdited = System::ExplicitCast<Aspose::Words::Document>(System::ExplicitCast<Aspose::Words::Node>(docOriginal)->Clone(true));
System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = docEdited->get_FirstSection()->get_Body()->get_FirstParagraph();

firstParagraph->get_Runs()->idx_get(0)->set_Text(u"hello world! this is the first paragraph, after editing.");
firstParagraph->get_ParagraphFormat()->set_Style(docEdited->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1));
(System::ExplicitCast<Aspose::Words::Notes::Footnote>(docEdited->GetChild(Aspose::Words::NodeType::Footnote, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(1)->set_Text(u"Edited endnote text.");
(System::ExplicitCast<Aspose::Words::Tables::Table>(docEdited->GetChild(Aspose::Words::NodeType::Table, 0, true)))->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited Cell 2 contents");
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(docEdited->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited textbox contents");
(System::ExplicitCast<Aspose::Words::Fields::FieldDate>(docEdited->get_Range()->get_Fields()->idx_get(0)))->set_UseLunarCalendar(true);
(System::ExplicitCast<Aspose::Words::Comment>(docEdited->GetChild(Aspose::Words::NodeType::Comment, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited comment.");
docEdited->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited header contents.");

// Belgeleri karşılaştırmak, düzenlenen belgede yapılan her düzenleme için bir revizyon oluşturur.
// Bir CompareOptions nesnesi, revizyonları bastırabilen bir dizi bayrağa sahiptir
// her ilgili öğe türü üzerinde, değişikliklerini etkili bir şekilde yok sayar.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_CompareMoves(false);
compareOptions->set_IgnoreFormatting(false);
compareOptions->set_IgnoreCaseChanges(false);
compareOptions->set_IgnoreComments(false);
compareOptions->set_IgnoreTables(false);
compareOptions->set_IgnoreFields(false);
compareOptions->set_IgnoreFootnotes(false);
compareOptions->set_IgnoreTextboxes(false);
compareOptions->set_IgnoreHeadersAndFooters(false);
compareOptions->set_Target(Aspose::Words::Comparing::ComparisonTargetType::New);

docOriginal->Compare(docEdited, u"John Doe", System::DateTime::get_Now(), compareOptions);
docOriginal->Save(get_ArtifactsDir() + u"Revision.CompareOptions.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
