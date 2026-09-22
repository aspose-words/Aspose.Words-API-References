---
title: "Aspose::Words::Paragraph::JoinRunsWithSameFormatting yöntemi"
linktitle: "JoinRunsWithSameFormatting"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::JoinRunsWithSameFormatting yöntemi. Paragraftaki aynı biçimlendirmeye sahip koşulları C++ içinde birleştirir."
type: docs
weight: 31000
url: /tr/cpp/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph::JoinRunsWithSameFormatting() method


Paragrafta aynı biçimlendirmeye sahip koşuları birleştirir.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting()
```


### ReturnValue

Gerçekleştirilen birleştirme sayısı. **N** ardışık run birleştirildiğinde, **N - 1** birleştirme olarak sayılır.

## Örnekler



Gereksiz koşulları birleştirerek paragrafları nasıl basitleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Paragrafa dört koşul metni ekleyin.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");
builder->Write(u"Run 3. ");
builder->Write(u"Run 4. ");

// Bu belgeyi Microsoft Word'de açarsak, paragraf tek bir kesintisiz metin gövdesi gibi görünecek.
// Ancak aynı biçimlendirmeye sahip dört ayrı koşuldan oluşacak. Bu tür parçalanmış paragraflar
// Microsoft Word'de bir paragrafın bölümlerini birçok kez manuel olarak düzenlediğimizde ortaya çıkabilir.
System::SharedPtr<Aspose::Words::Paragraph> para = builder->get_CurrentParagraph();

ASSERT_EQ(4, para->get_Runs()->get_Count());

// Son koşulun stilini değiştirerek onu ilk üçünden ayırın.
para->get_Runs()->idx_get(3)->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Emphasis);

// "JoinRunsWithSameFormatting" yöntemini çalıştırarak belgenin içeriğini optimize edebiliriz
// benzer koşulları birleştirerek sayısını azaltıp tek bir koşul haline getiririz.
// Bu yöntem ayrıca bu yöntemin birleştirdiği koşul sayısını da döndürür.
// Bu iki birleştirme, Koşul #1, #2 ve #3'ü birleştirmek için gerçekleşti,
// Run #4'ü dışarıda bırakarak, çünkü uyumsuz bir stile sahiptir.
ASSERT_EQ(2, para->JoinRunsWithSameFormatting());

// Kalan run sayısı, orijinal sayıya eşit olacaktır
// "JoinRunsWithSameFormatting" yöntemi tarafından gerçekleştirilen run birleştirme sayısı çıkarılır.
ASSERT_EQ(2, para->get_Runs()->get_Count());
ASSERT_EQ(u"Run 1. Run 2. Run 3. ", para->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"Run 4. ", para->get_Runs()->idx_get(1)->get_Text());
```

## Ayrıca Bakınız

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) method


Paragrafta aynı biçimlendirmeye sahip koşuları birleştirir.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr<Aspose::Words::JoinRunsOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| seçenekler | const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\& | Ek seçenekler |

### ReturnValue

Gerçekleştirilen birleştirme sayısı. **N** ardışık run birleştirildiğinde, **N - 1** birleştirme olarak sayılır.

## Örnekler



Aynı biçimlendirmeye sahip çalıştırmaları, gereksiz ve önemsiz öznitelikleri yok sayarak nasıl birleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Görünür biçimlendirmesi aynı ancak bazı içsel farklılıkları olan çalıştırmalar oluşturun.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// Birleştirmeden önce çalıştırmaları doğrulayın.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// Birleştirme sırasında gereksiz ve önemsiz öznitelikleri yok saymak için seçenekleri yapılandırın.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// Görünümü etkilemeyen gereksiz çalıştırma özelliklerini yok sayın.
options->set_IgnoreInsignificant(true);
// Yalnızca boşluk içeren çalıştırmalar gibi önemsiz farkları yok sayın.

// Genişletilmiş seçenekleri kullanarak aynı görünür biçimlendirmeye sahip run'ları birleştirin.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// Run'ların başarıyla birleştirildiğini doğrulayın.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## Ayrıca Bakınız

* Class [JoinRunsOptions](../../joinrunsoptions/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
