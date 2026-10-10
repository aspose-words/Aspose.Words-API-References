---
title: "Aspose::Words::StyleCollection sınıfı"
linktitle: "StyleCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::StyleCollection sınıfı. Bir belge içinde yerleşik ve kullanıcı tanımlı stilleri temsil eden Style nesnelerinin bir koleksiyonudur. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 65000
url: /tr/cpp/aspose.words/stylecollection/
---
## StyleCollection class


Bir belge içinde yerleşik ve kullanıcı tanımlı stilleri temsil eden [Style](../style/) nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/) belge makalesini ziyaret edin.

```cpp
class StyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Style>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(Aspose::Words::StyleType, const System::String\&) | Yeni bir kullanıcı tanımlı stil oluşturur ve koleksiyona ekler. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Bu koleksiyona bir stili kopyalar. |
| [ClearQuickStyleGallery](./clearquickstylegallery/)() | Hızlı [Style](../style/) Galeri panelinden tüm stilleri kaldırır. |
| [get_Count](./get_count/)() | Koleksiyondaki stil sayısını alır. |
| [get_DefaultFont](./get_defaultfont/)() | Belgenin varsayılan metin biçimlendirmesini alır. |
| [get_DefaultParagraphFormat](./get_defaultparagraphformat/)() | Belgenin varsayılan paragraf biçimlendirmesini alır. |
| [get_Document](./get_document/)() const | Sahip belgeyi alır. |
| [GetEnumerator](./getenumerator/)() override | Stilleri adlarının alfabetik sırasına göre sıralayacak bir enumerator nesnesi alır. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Bir stili adına ya da takma adına göre alır. |
| [idx_get](./idx_get/)(Aspose::Words::StyleIdentifier) | Yerel bağımsız tanımlayıcısına göre yerleşik bir stili alır. |
| [idx_get](./idx_get/)(int32_t) | Bir stili indeksine göre alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
