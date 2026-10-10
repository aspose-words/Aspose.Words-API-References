---
title: "Aspose::Words::Document::Compare yöntemi"
linktitle: "Compare"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::Compare yöntemi. Bu belgeyi başka bir belgeyle karşılaştırır ve değişiklikleri C++'da düzenleme ve biçim revizyonları (Revision) sayısı olarak üretir."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/document/compare/
---
## Document::Compare(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime) method


Bu belgeyi başka bir belgeyle karşılaştırır ve değişiklikleri düzenleme ve biçim revizyonları sayısı olarak üretir [Revision](../../revision/).

```cpp
void Aspose::Words::Document::Compare(const System::SharedPtr<Aspose::Words::Document> &document, const System::String &author, System::DateTime dateTime)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| document | const System::SharedPtr\<Aspose::Words::Document\>\& | Karşılaştırılacak [Document](../). |
| yazar | const System::String\& | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | System::DateTime | Revizyonlar için kullanılacak tarih ve saat. |
## Açıklamalar



Belgelerin karşılaştırmadan önce revizyonları olmamalıdır.
## Örnekler



Belgelerin nasıl karşılaştırılacağını gösterir.
```cpp
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// Revizyonlu belgeleri karşılaştırmak bir istisna fırlatır.
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// Karşılaştırmadan sonra, orijinal belge yeni bir revizyon kazanacaktır
// düzenlenmiş belgede farklı olan her öğe için.
for (auto&& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << System::String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType()) << std::endl;
    std::cout << System::String::Format(u"\tChanged text: \"{0}\"", r->get_ParentNode()->GetText()) << std::endl;
}

// Bu revizyonları kabul etmek, orijinal belgeyi düzenlenmiş belgeye dönüştürecektir.
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## Ayrıca Bakınız

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Compare(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Bu belgeyi başka bir belgeyle karşılaştırır ve değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir [Revision](../../revision/). [CompareOptions](../../../aspose.words.comparing/compareoptions/) kullanarak karşılaştırma seçeneklerini belirtmeye olanak tanır.

```cpp
void Aspose::Words::Document::Compare(const System::SharedPtr<Aspose::Words::Document> &document, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &options)
```


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

* Class [Document](../)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
