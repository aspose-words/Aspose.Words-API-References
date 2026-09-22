---
title: "Aspose::Words::ParagraphFormat::get_StyleIdentifier yöntemi"
linktitle: "get_StyleIdentifier"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_StyleIdentifier yöntemi. Bu biçimlendirmeye uygulanan paragraf stilinin bölge bağımsız stil tanımlayıcısını alır veya ayarlar C++'ta."
type: docs
weight: 36000
url: /tr/cpp/aspose.words/paragraphformat/get_styleidentifier/
---
## ParagraphFormat::get_StyleIdentifier method


Bu biçimlendirmeye uygulanan paragraf stilinin yerel bağımsız stil tanımlayıcısını alır veya ayarlar.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::ParagraphFormat::get_StyleIdentifier()
```


## Örnekler



Başlık stillerini giriş olarak kullanarak bir belgeye İçindekiler Tablosu (TOC) eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgenin ilk sayfası için bir içindekiler tablosu ekleyin.
// Tabloyu, 1 ila 3 seviyelerindeki başlıklarla paragraf alacak şekilde yapılandırın.
// Ayrıca, girdilerini bizi yönlendirecek hiperlinkler olarak ayarlayın
// Microsoft Word'de sol tıklandığında başlığın konumuna.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// İçindekiler tablosunu, başlık stilleriyle paragraflar ekleyerek doldurun.
// 1 ile 3 arasında bir seviyeye sahip her başlık, tabloda bir giriş oluşturur.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// İçindekiler tablosu, güncel bir sonuç göstermek için güncellenmesi gereken bir tür alanıdır.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```

## Ayrıca Bakınız

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
