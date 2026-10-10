---
title: "Aspose::Words::InlineStory::EnsureMinimum metodu"
linktitle: "EnsureMinimum"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::InlineStory::EnsureMinimum yöntemi. Son çocuk bir paragraf değilse, C++'ta bir boş paragraf oluşturur ve ekler."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/inlinestory/ensureminimum/
---
## InlineStory::EnsureMinimum method


Son çocuk bir paragraf değilse, boş bir paragraf oluşturur ve ekler.

```cpp
void Aspose::Words::InlineStory::EnsureMinimum()
```


## Örnekler



[InlineStory](../) düğümlerinin nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, nullptr);

// Tablo düğümlerinin en az bir hücreye sahip olmasını sağlayan "EnsureMinimum()" yöntemi vardır.
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
table->EnsureMinimum();

// Bir dipnotun içine bir tablo yerleştirebiliriz, bu da tablonun referans sayfasının altbilgisinde görünmesini sağlar.
ASSERT_EQ(0, footnote->get_Tables()->get_Count());
footnote->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
ASSERT_EQ(1, footnote->get_Tables()->get_Count());
ASSERT_EQ(Aspose::Words::NodeType::Table, footnote->get_LastChild()->get_NodeType());

// Bir InlineStory'nin de "EnsureMinimum()" yöntemi vardır, ancak bu durumda,
// düğümün son çocuğunun bir paragraf olmasını sağlar,
// Microsoft Word'de kolayca tıklayıp metin yazabilmemiz için.
footnote->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, footnote->get_LastChild()->get_NodeType());

// Küçük üst simge sayı olan ankrajın görünümünü düzenleyin,
// dipnota işaret eden ana metinde.
footnote->get_Font()->set_Name(u"Arial");
footnote->get_Font()->set_Color(System::Drawing::Color::get_Green());

// Tüm inline hikaye düğümlerinin kendi hikaye türleri vardır.
ASSERT_EQ(Aspose::Words::StoryType::Footnotes, footnote->get_StoryType());

// Bir yorum, başka bir inline hikaye türüdür.
auto comment = System::ExplicitCast<Aspose::Words::Comment>(builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J. D.", System::DateTime::get_Now())));

// Satır içi hikaye düğümünün üst paragrafı, ana belge gövdesinden gelen paragraf olacaktır.
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), comment->get_ParentParagraph());

// Ancak, son paragraf yorum metni içeriğinden gelen paragraftır,
// bu, bir konuşma balonunda ana belge gövdesinin dışında olacaktır.
// Bir yorum varsayılan olarak hiçbir alt düğüme sahip olmayacaktır,
// bu yüzden burada da bir paragraf yerleştirmek için EnsureMinimum() yöntemini uygulayabiliriz.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_LastParagraph()));
comment->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, comment->get_LastChild()->get_NodeType());

// Bir paragraf elde ettiğimizde, oluşturucuyu hareket ettirerek bunu yapabilir ve yorumumuzu yazabiliriz.
builder->MoveTo(comment->get_LastParagraph());
builder->Write(u"My comment.");

ASSERT_EQ(Aspose::Words::StoryType::Comments, comment->get_StoryType());

doc->Save(get_ArtifactsDir() + u"InlineStory.InsertInlineStoryNodes.docx");
```

## Ayrıca Bakınız

* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
