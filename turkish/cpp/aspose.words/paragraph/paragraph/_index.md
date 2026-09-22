---
title: "Aspose::Words::Paragraph::Paragraph yapıcı"
linktitle: "Paragraph"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::Paragraph yapıcı. C++'da Paragraph sınıfının yeni bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/paragraph/paragraph/
---
## Paragraph::Paragraph constructor


[Paragraph](../) sınıfının yeni bir örneğini başlatır.

```cpp
Aspose::Words::Paragraph::Paragraph(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Sahip belge. |
## Açıklamalar


[Paragraph](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve [ParentNode](../../node/get_parentnode/) **null**'dır.

Belgeye [Paragraph](../) eklemek için, paragrafın eklenmesini istediğiniz hikayede [InsertAfter1()</see> veya <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) kullanın.

## Örnekler



Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge bir bölüm, bir gövde ve bir paragraf içerir.
// "RemoveAllChildren" yöntemini çağırarak bu düğümlerin tümünü kaldırın,
// ve hiçbir çocuğu olmayan bir belge düğümü elde edin.
doc->RemoveAllChildren();

// Bu belge artık içerik ekleyebileceğimiz birleşik alt düğümlere sahip değil.
// Eğer düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// İlk olarak yeni bir bölüm oluşturun ve ardından kök belge düğümüne çocuk olarak ekleyin.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Bölüm için bazı sayfa ayarı özelliklerini ayarlayın.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Bir bölüm bir gövdeye ihtiyaç duyar, bu gövde tüm içeriğini barındırır ve gösterir
// sayfada bölümün başlığı ile altbilgisi arasındaki alanda.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından onu gövdenin bir çocuğu olarak ekleyin.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Son olarak, belgeye içerik ekleyin. Bir run oluşturun,
// Görünümünü ve içeriğini ayarlayın, ardından onu paragrafın bir çocuğu olarak ekleyin.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Ayrıca Bakınız

* Class [DocumentBase](../../documentbase/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
