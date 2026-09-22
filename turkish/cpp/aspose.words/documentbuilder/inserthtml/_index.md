---
title: "Aspose::Words::DocumentBuilder::InsertHtml metodu"
linktitle: "InsertHtml"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertHtml metodu. C++'ta bir HTML dizesini belgeye ekler."
type: docs
weight: 37000
url: /tr/cpp/aspose.words/documentbuilder/inserthtml/
---
## DocumentBuilder::InsertHtml(const System::String\&) method


Belgeye bir HTML dizesi ekler.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| html | const System::String\& | Belgeye eklemek için bir HTML dizesi. |

## Örnekler



Bir belge builder'ı kullanarak html içeriğini belgeye nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const System::String html = System::String(u"<p align='right'>Paragraph right</p>") + u"<b>Implicit paragraph left</b>" + u"<div align='center'>Div center</div>" + u"<h1 align='left'>Heading 1 left.</h1>";

builder->InsertHtml(html);

// HTML kodunu eklemek, her öğenin biçimlendirmesini eşdeğer belge metni biçimlendirmesine dönüştürür.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(u"Paragraph right", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Implicit paragraph left", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_TRUE(paragraphs->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_Bold());

ASSERT_EQ(u"Div center", paragraphs->idx_get(2)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Heading 1 left.", paragraphs->idx_get(3)->GetText().Trim());
ASSERT_EQ(u"Heading 1", paragraphs->idx_get(3)->get_ParagraphFormat()->get_Style()->get_Name());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtml.docx");
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, Aspose::Words::HtmlInsertOptions) method


Belgeye bir HTML dizesi ekler. Ek seçenekleri belirtmeye izin verir.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, Aspose::Words::HtmlInsertOptions options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| html | const System::String\& | Belgeye eklemek için bir HTML dizesi. |
| seçenekler | Aspose::Words::HtmlInsertOptions | HTML dizesi eklendiğinde kullanılan seçenekler. |

## Ayrıca Bakınız

* Enum [HtmlInsertOptions](../../htmlinsertoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, bool) method


Belgeye bir HTML dizesi ekler.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, bool useBuilderFormatting)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| html | const System::String\& | Belgeye eklemek için bir HTML dizesi. |
| useBuilderFormatting | bool | HTML'den içe aktarılan metin için temel biçimlendirme olarak [DocumentBuilder](../) içinde belirtilen biçimlendirmenin kullanılıp kullanılmadığını gösteren bir değer. |
## Açıklamalar


Bu metodu bir HTML parçacığı veya tam bir HTML belge eklemek için kullanabilirsiniz.

*useBuilderFormatting* **false** olduğunda, [DocumentBuilder](../) biçimlendirmesi yok sayılır ve eklenen metnin biçimlendirmesi varsayılan HTML biçimlendirmesine dayanır. Sonuç olarak, metin tarayıcılarda render edildiği gibi görünür.

*useBuilderFormatting* **true** olduğunda, eklenen metnin biçimlendirmesi [DocumentBuilder](../) biçimlendirmesine dayanır ve metin [Write()](../) ile eklenmiş gibi görünür.

## Örnekler



HTML içeriği eklerken bir belge builder'ının biçimlendirmesinin nasıl uygulanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Builder için bir metin hizalaması ayarlayın, belirli bir hizalama ile bir HTML paragrafı ve hizalama olmadan bir paragraf ekleyin.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Distributed);
builder->InsertHtml(System::String(u"<p align='right'>Paragraph 1.</p>") + u"<p>Paragraph 2.</p>", useBuilderFormatting);

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// İlk paragrafta bir hizalama belirtilmiştir. InsertHtml HTML kodunu ayrıştırdığında,
// HTML kodunda bulunan paragraf hizalama değeri her zaman belge builder'ının değerini geçersiz kılar.
ASSERT_EQ(u"Paragraph 1.", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

// İkinci paragrafta hizalama belirtilmemiştir. Hizalama değeri doldurulabilir
// InsertHtml metoduna gönderdiğimiz bayrağa bağlı olarak builder'ın değeriyle.
ASSERT_EQ(u"Paragraph 2.", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(useBuilderFormatting ? Aspose::Words::ParagraphAlignment::Distributed : Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtmlWithFormatting.docx");
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
