---
title: "Aspose::Words::DocumentBuilder::DocumentBuilder yapıcı"
linktitle: "DocumentBuilder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::DocumentBuilder yapıcı. C++'da bu sınıfın yeni bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder::DocumentBuilder() constructor


Bu sınıfın yeni bir örneğini başlatır.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder()
```


## Örnekler



[DocumentBuilder](../) kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yazı tipi biçimlendirmesini belirtin, ardından metin ekleyin.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&) constructor


Bu sınıfın yeni bir örneğini başlatır.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | Eklenecek [Document](../../document/) nesnesi. |

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

* Class [Document](../../document/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


Bu sınıfın yeni bir örneğini başlatır.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | Eklenecek [Document](../../document/) nesnesi. |
| seçenekler | const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\& | Belge oluşturma süreci için ek seçenekler. |

## Örnekler



Tablo biçimlendirmesini sonraki içerik için nasıl yok sayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Tablonun önüne içerik ekler.
// Varsayılan yazı tipi boyutu 12'dir.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Tablonun içindeki yazı tipi boyutunu değiştirir.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// ContextTableFormatting true ise, tablo biçimlendirmesi sonraki içeriğe uygulanmaz.
// ContextTableFormatting false ise, tablo biçimlendirmesi sonraki içeriğe uygulanır.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Ayrıca Bakınız

* Class [Document](../../document/)
* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


Bu sınıfın yeni bir örneğini başlatır.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```


## Örnekler



Tablo biçimlendirmesini sonraki içerik için nasıl yok sayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Tablonun önüne içerik ekler.
// Varsayılan yazı tipi boyutu 12'dir.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Tablonun içindeki yazı tipi boyutunu değiştirir.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// ContextTableFormatting true ise, tablo biçimlendirmesi sonraki içeriğe uygulanmaz.
// ContextTableFormatting false ise, tablo biçimlendirmesi sonraki içeriğe uygulanır.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Ayrıca Bakınız

* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
