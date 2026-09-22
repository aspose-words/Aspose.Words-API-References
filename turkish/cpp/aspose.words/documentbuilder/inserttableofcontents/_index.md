---
title: "Aspose::Words::DocumentBuilder::InsertTableOfContents method"
linktitle: "InsertTableOfContents"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertTableOfContents yöntemi. C++'ta belgeye bir TOC (içindekiler tablosu) alanı ekler."
type: docs
weight: 48000
url: /tr/cpp/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder::InsertTableOfContents method


Belgeye bir TOC (içindekiler tablosu) alanı ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertTableOfContents(const System::String &switches)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| anahtarlar | const System::String\& | TOC alanı anahtarları. |
## Açıklamalar


Bu yöntem, mevcut konumda belgeye bir TOC (içindekiler tablosu) alanı ekler.

Word belgesindeki bir içindekiler tablosu çeşitli yollarla oluşturulabilir ve çeşitli seçeneklerle biçimlendirilebilir. Tablonun Microsoft Word tarafından oluşturulma ve görüntülenme şekli alan anahtarlarıyla kontrol edilir.

Anahtarları belirtmenin en kolay yolu, Insert->Reference->Index ve [Tables](../../../aspose.words.tables/) menüsünü kullanarak bir Word belgesine içindekiler tablosu eklemek ve yapılandırmaktır; ardından alan kodlarının görüntülenmesini açarak anahtarları görebilirsiniz. Microsoft Word'de alan kodlarının görüntülenmesini açıp kapatmak için Alt+F9 tuşuna basabilirsiniz.

Örneğin, bir içindekiler tablosu oluşturduktan sonra, belgeye aşağıdaki alan eklenir: **%{ TOC \o \"1-3\" \h \z }**. **%\o \"1-3\" \h \z** ifadesini kopyalayıp anahtarlar parametresi olarak kullanabilirsiniz.

Not edin ki [InsertTableOfContents()](../) yalnızca bir TOC alanı ekleyecek, ancak içindekiler tablosunu aslında oluşturmayacaktır. İçindekiler tablosu, alan güncellendiğinde Microsoft Word tarafından oluşturulur.

Bu yöntemi kullanarak bir içindekiler tablosu eklerseniz ve ardından dosyayı Microsoft Word'de açarsanız, TOC alanı henüz güncellenmediği için içindekiler tablosunu görmezsiniz.

Microsoft Word'de, bir belge açıldığında alanlar otomatik olarak güncellenmez, ancak F9 tuşuna basarak istediğiniz zaman bir belgedeki alanları güncelleyebilirsiniz.

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

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
