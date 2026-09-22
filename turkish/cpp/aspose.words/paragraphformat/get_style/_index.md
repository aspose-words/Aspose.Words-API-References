---
title: "Aspose::Words::ParagraphFormat::get_Style yöntemi"
linktitle: "get_Style"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_Style yöntemi. Bu biçimlendirmeye uygulanan paragraf stilini alır veya ayarlar C++'ta."
type: docs
weight: 35000
url: /tr/cpp/aspose.words/paragraphformat/get_style/
---
## ParagraphFormat::get_Style method


Bu biçimlendirmeye uygulanan paragraf stilini alır veya ayarlar.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::ParagraphFormat::get_Style()
```


## Örnekler



Liste biçimlendirmeli bir paragraf stilinin nasıl oluşturulup kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Özel bir paragraf stili oluştur.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Bir liste oluşturun ve bu stili kullanan paragrafların bu listeyi kullanmasını sağlayın.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Paragraf stilini belge oluşturucunun mevcut paragrafına uygulayın ve ardından metin ekleyin.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Belge oluşturucunun stilini liste biçimlendirmesi olmayan bir stile değiştirin ve başka bir paragraf yazın.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Ayrıca Bakınız

* Class [Style](../../style/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
