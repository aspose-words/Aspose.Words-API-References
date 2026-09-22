---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_EndCharacterFont yöntemi"
linktitle: "get_EndCharacterFont"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_EndCharacterFont yöntemi. SDT'ye girilen metnin son karakterine uygulanacak yazı tipi biçimlendirmesi C++'ta."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/get_endcharacterfont/
---
## StructuredDocumentTag::get_EndCharacterFont method


[Font](../../../aspose.words/font/) formatting that will be applied to the last character of text entered into **SDT**.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Markup::StructuredDocumentTag::get_EndCharacterFont()
```


## Örnekler



Düz metin kutusunda bir yapılandırılmış belge etiketi oluşturmayı ve görünümünü değiştirmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Düz metin içerecek bir yapılandırılmış belge etiketi oluşturun.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Microsoft Word'de yapılandırılmış belge etiketinin üzerine fareyle geldiğinizde görünen çerçevenin başlığını ve rengini ayarlayın.
tag->set_Title(u"My plain text");
tag->set_Color(System::Drawing::Color::get_Magenta());

// Bu yapılandırılmış belge etiketi için elde edilebilen bir etiket ayarlayın
// "tag" adlı bir XML öğesi olarak, aşağıdaki dizeyi "@val" özniteliğinde içerir.
tag->set_Tag(u"MyPlainTextSDT");

// Her yapılandırılmış belge etiketinin rastgele benzersiz bir kimliği vardır.
ASSERT_TRUE(tag->get_Id() > 0);

// Yapılandırılmış belge etiketinin içindeki metin için yazı tipini ayarlayın.
tag->get_ContentsFont()->set_Name(u"Arial");

// Yapılandırılmış belge etiketinin sonundaki metin için yazı tipini ayarlayın.
// Ok tuşlarıyla etiketten çıktıktan sonra belge gövdesine yazdığımız tüm metin bu yazı tipini kullanacaktır.
tag->get_EndCharacterFont()->set_Name(u"Arial Black");

// Varsayılan olarak, bu false'tur ve bir yapılandırılmış belge etiketi içinde Enter tuşuna basmak hiçbir şey yapmaz.
// True olarak ayarlandığında, yapılandırılmış belge etiketimiz birden fazla satır içerebilir.

// "Multiline" özelliğini "false" olarak ayarlayın, böylece yalnızca içeriklerin
// bu yapılandırılmış belge etiketinin tek bir satırda olmasını sağlayın.
// "Multiline" özelliğini "true" olarak ayarlayın, böylece etiket birden fazla satır içerik barındırabilir.
tag->set_Multiline(true);

// "Appearance" özelliğini "SdtAppearance.Tags" olarak ayarlayın, böylece içerik etrafında etiketler gösterilir.
// Varsayılan olarak yapılandırılmış belge etiketi BoundingBox olarak gösterilir.
tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

// Yapılandırılmış belge etiketimizin bir klonunu yeni bir paragrafta ekleyin.
auto tagClone = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(System::ExplicitCast<Aspose::Words::Node>(tag)->Clone(true));
builder->InsertParagraph();
builder->InsertNode(tagClone);

// "RemoveSelfOnly" yöntemini kullanarak bir yapılandırılmış belge etiketini kaldırın, ancak içeriğini belgede tutun.
tagClone->RemoveSelfOnly();

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlainText.docx");
```

## Ayrıca Bakınız

* Class [Font](../../../aspose.words/font/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
