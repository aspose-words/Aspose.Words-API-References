---
title: "Aspose::Words::Comparing::CompareOptions sınıfı"
linktitle: "CompareOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comparing::CompareOptions sınıfı. Belge karşılaştırma işlemi için ek seçenekler seçmenize olanak tanır. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.comparing/compareoptions/
---
## CompareOptions class


Belge karşılaştırma işlemi için ek seçenekler seçmeye izin verir. Daha fazla bilgi için, [Compare Documents](https://docs.aspose.com/words/cpp/compare-documents/) dokümantasyon makalesini ziyaret edin.

```cpp
class CompareOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [CompareOptions](./compareoptions/)() |  |
| [get_AdvancedOptions](./get_advancedoptions/)() const | Daha kesin karşılaştırma çıktısı üretmeye yardımcı olabilecek gelişmiş karşılaştırma seçeneklerini belirtir. |
| [get_CompareMoves](./get_comparemoves/)() const | İki belge arasındaki farkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [get_Granularity](./get_granularity/)() const | Değişikliklerin karakter bazında mı yoksa kelime bazında mı izleneceğini belirtir. |
| [get_IgnoreCaseChanges](./get_ignorecasechanges/)() const | True, belge karşılaştırmasının büyük/küçük harfe duyarsız olduğunu gösterir. |
| [get_IgnoreComments](./get_ignorecomments/)() const | Yorumlardaki farkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() | DrawingML benzersiz kimliğindeki farkı göz ardı edip etmeyeceğini belirtir. |
| [get_IgnoreFields](./get_ignorefields/)() const | Alanlardaki farkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Dipnot ve son notlardaki farkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [get_IgnoreFormatting](./get_ignoreformatting/)() const | True, biçimlendirmelerin yok sayıldığını gösterir. |
| [get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/)() const | True, üstbilgi ve altbilgi içeriğinin yok sayıldığını gösterir. |
| [get_IgnoreTables](./get_ignoretables/)() const | Tablolarda bulunan verilerdeki farkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [get_IgnoreTextboxes](./get_ignoretextboxes/)() const | Metin kutularında bulunan verilerdeki farkların karşılaştırılıp karşılaştırılmayacağını belirtir. |
| [get_Target](./get_target/)() const | Karşılaştırma sırasında hedef olarak kullanılacak belgeyi belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CompareMoves](./set_comparemoves/)(bool) | Ayarlayıcı: [Aspose::Words::Comparing::CompareOptions::get_CompareMoves](./get_comparemoves/). |
| [set_Granularity](./set_granularity/)(Aspose::Words::Comparing::Granularity) | Ayarlayıcı: [Aspose::Words::Comparing::CompareOptions::get_Granularity](./get_granularity/). |
| [set_IgnoreCaseChanges](./set_ignorecasechanges/)(bool) | Ayarlayıcı: [Aspose::Words::Comparing::CompareOptions::get_IgnoreCaseChanges](./get_ignorecasechanges/). |
| [set_IgnoreComments](./set_ignorecomments/)(bool) | Ayarlayıcı: [Aspose::Words::Comparing::CompareOptions::get_IgnoreComments](./get_ignorecomments/). |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Ayarlayıcı: [Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Ayarlayıcı: [Aspose::Words::Comparing::CompareOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Ayarlayıcı: [Aspose::Words::Comparing::CompareOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreFormatting](./set_ignoreformatting/)(bool) | Ayarlayıcı: [Aspose::Words::Comparing::CompareOptions::get_IgnoreFormatting](./get_ignoreformatting/). |
| [set_IgnoreHeadersAndFooters](./set_ignoreheadersandfooters/)(bool) | Ayarlayıcı [Aspose::Words::Comparing::CompareOptions::get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/). |
| [set_IgnoreTables](./set_ignoretables/)(bool) | Ayarlayıcı [Aspose::Words::Comparing::CompareOptions::get_IgnoreTables](./get_ignoretables/). |
| [set_IgnoreTextboxes](./set_ignoretextboxes/)(bool) | Ayarlayıcı [Aspose::Words::Comparing::CompareOptions::get_IgnoreTextboxes](./get_ignoretextboxes/). |
| [set_Target](./set_target/)(Aspose::Words::Comparing::ComparisonTargetType) | Ayarlayıcı [Aspose::Words::Comparing::CompareOptions::get_Target](./get_target/). |
| static [Type](./type/)() |  |

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
