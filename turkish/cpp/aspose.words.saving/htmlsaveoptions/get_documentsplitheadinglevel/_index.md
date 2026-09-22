---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel yöntemi"
linktitle: "get_DocumentSplitHeadingLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel yöntemi. Belgenin bölüneceği en yüksek başlık seviyesini belirtir. Varsayılan değer C++'da %2'dir."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitheadinglevel/
---
## HtmlSaveOptions::get_DocumentSplitHeadingLevel method


Belgenin bölüneceği en yüksek başlık seviyesini belirtir. Varsayılan değer **%2**'dir.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel() const
```

## Açıklamalar


[DocumentSplitCriteria](../get_documentsplitcriteria/) [HeadingParagraph](../../documentsplitcriteria/) içerdiğinde ve bu özellik 1 ile 9 arasında bir değere ayarlandığında, belge **Heading 1**, **Heading 2**, **Heading 3** vb. stillerle biçimlendirilmiş paragraflarda, belirtilen başlık seviyesine kadar bölünecektir.

Varsayılan olarak, yalnızca **Heading 1** ve **Heading 2** paragrafları belgenin bölünmesine neden olur. Bu özelliği sıfıra ayarlamak, belgenin başlık paragraflarında hiç bölünmemesini sağlar.

## Örnekler



Bir çıktı HTML belgesini başlıklara göre birkaç bölüme nasıl bölüneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// "Heading" stiliyle biçimlendirdiğimiz her paragraf bir başlık olarak hizmet edebilir.
// Her başlık, başlık stilinin sayısına göre belirlenen bir başlık seviyesine de sahip olabilir.
// Aşağıdaki başlıklar 1-3 seviyelerindedir.
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #1");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #2");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #3");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #4");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #5");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #6");

// Bir HtmlSaveOptions nesnesi oluşturun ve bölme kriterini "HeadingParagraph" olarak ayarlayın.
// Bu kriterler, "Heading" stilli paragraflarda belgeyi birkaç daha küçük belgeye bölecek,
// ve her belgeyi yerel dosya sisteminde ayrı bir HTML dosyası olarak kaydedecek.
// Ayrıca belgeyi 2 seviyeye bölmek için maksimum başlık seviyesini ayarlayacağız.
// Belgeyi kaydetmek, onu 1 ve 2 seviyesindeki başlıklarda bölecek, ancak 3 ile 9 arasındaki seviyelerde bölmeyecektir.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);
options->set_DocumentSplitHeadingLevel(2);

// Belgemizde 1 - 2 seviyelerinde dört başlık var. Bu başlıklardan biri olmayacak
// belgenin başında olduğu için bir bölme noktasıdır.
// Kaydetme işlemi belgemizi üç yerde bölerek dört daha küçük belgeye ayıracaktır.
doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html");

ASSERT_EQ(u"Heading #1", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-01.html");

ASSERT_EQ(System::String(u"Heading #2\r") + u"Heading #3", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-02.html");

ASSERT_EQ(u"Heading #4", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-03.html");

ASSERT_EQ(System::String(u"Heading #5\r") + u"Heading #6", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
