---
title: "Aspose::Words::Style class"
linktitle: "Style"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style sınıfı. Tek bir yerleşik veya kullanıcı tanımlı stili temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 64000
url: /tr/cpp/aspose.words/style/
---
## Style class


Tek bir yerleşik veya kullanıcı tanımlı stili temsil eder. Daha fazla bilgi edinmek için, [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/) belgeler makalesini ziyaret edin.

```cpp
class Style : public Aspose::Words::IParaAttrSource,
              public Aspose::Words::IRunAttrSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Belirtilen stil ile karşılaştırır. Styles Istds yalnızca yerleşik stiller için karşılaştırılır. Stil varsayılanları karşılaştırmaya dahil edilmez. Temel stil, bağlı stil ve sonraki paragraf stili özyinelemeli olarak karşılaştırılır. |
| [get_Aliases](./get_aliases/)() | Bu stilin tüm takma adlarını alır. Stil takma ada sahip değilse boş bir dize dizisi döndürülür. |
| [get_AutomaticallyUpdate](./get_automaticallyupdate/)() const | Bu stilin uygun değere göre otomatik olarak yeniden tanımlanıp tanımlanmayacağını belirtir. |
| [get_BaseStyleName](./get_basestylename/)() | Bu stilin dayandığı stilin adını alır/ayar. |
| [get_BuiltIn](./get_builtin/)() | Bu stil MS Word'deki yerleşik stillerden biri ise doğru. |
| [get_Document](./get_document/)() | Sahip belgeyi alır. |
| [get_Font](./get_font/)() | Stilin karakter biçimlendirmesini alır. |
| [get_IsHeading](./get_isheading/)() | Stil yerleşik Başlık stillerinden biri olduğunda doğru. |
| [get_IsQuickStyle](./get_isquickstyle/)() const | Bu stilin MS Word UI içinde Hızlı [Style](./) galerisinde gösterilip gösterilmeyeceğini belirtir. |
| [get_LinkedStyleName](./get_linkedstylename/)() | Bu stile bağlı olan [Style](./) adını alır/ayar. Bağlı stil yoksa boş dize döndürür. |
| [get_List](./get_list/)() | Bu liste stilinin biçimlendirmesini tanımlayan listeyi alır. |
| [get_ListFormat](./get_listformat/)() | Bir paragraf stilinin liste biçimlendirme özelliklerine erişim sağlar. |
| [get_Locked](./get_locked/)() const | Bu stilin kilitli olup olmadığını belirtir. |
| [get_Name](./get_name/)() const | Stilin adını alır veya ayarlar. |
| [get_NextParagraphStyleName](./get_nextparagraphstylename/)() | Belirtilen stil ile biçimlendirilmiş bir paragraftan sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayar. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Stilin paragraf biçimlendirmesini alır. |
| [get_Priority](./get_priority/)() const | Stiller görev bölmesinde stilleri sıralama önceliğini temsil eden tam sayı değerini alır/ayar. |
| [get_SemiHidden](./get_semihidden/)() const | Stilin Styles galerisinden ve Styles görev bölmesinden gizlenip gizlenmediğini alır/ayarlar. |
| [get_StyleIdentifier](./get_styleidentifier/)() const | Yerel bağımsız bir yerleşik stil için stil tanımlayıcısını alır. |
| [get_Styles](./get_styles/)() const | Bu stilin ait olduğu stil koleksiyonunu alır. |
| [get_Type](./get_type/)() const | Stil tipini (paragraf veya karakter) alır. |
| [get_UnhideWhenUsed](./get_unhidewhenused/)() const | Geçerli belgede kullanılan stilin Styles galerisinden ve Styles görev bölmesinden gizlenip gizlenmediğini alır/ayarlar. Stil galerisinde gösterilmesi gerektiğinde doğru (true) olur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Belirtilen stili belgeden kaldırır. |
| [set_AutomaticallyUpdate](./set_automaticallyupdate/)(bool) | [Aspose::Words::Style::get_AutomaticallyUpdate](./get_automaticallyupdate/) için ayarlayıcı. |
| [set_BaseStyleName](./set_basestylename/)(const System::String\&) | [Aspose::Words::Style::get_BaseStyleName](./get_basestylename/) için ayarlayıcı. |
| [set_IsQuickStyle](./set_isquickstyle/)(bool) | [Aspose::Words::Style::get_IsQuickStyle](./get_isquickstyle/) için ayarlayıcı. |
| [set_LinkedStyleName](./set_linkedstylename/)(const System::String\&) | [Aspose::Words::Style::get_LinkedStyleName](./get_linkedstylename/) için ayarlayıcı. |
| [set_Locked](./set_locked/)(bool) | [Aspose::Words::Style::get_Locked](./get_locked/) için ayarlayıcı. |
| [set_Name](./set_name/)(const System::String\&) | [Aspose::Words::Style::get_Name](./get_name/) için ayarlayıcı. |
| [set_NextParagraphStyleName](./set_nextparagraphstylename/)(const System::String\&) | [Aspose::Words::Style::get_NextParagraphStyleName](./get_nextparagraphstylename/) için ayarlayıcı. |
| [set_Priority](./set_priority/)(int32_t) | [Aspose::Words::Style::get_Priority](./get_priority/) için ayarlayıcı. |
| [set_SemiHidden](./set_semihidden/)(bool) | [Aspose::Words::Style::get_SemiHidden](./get_semihidden/) için ayarlayıcı. |
| [set_UnhideWhenUsed](./set_unhidewhenused/)(bool) | [Aspose::Words::Style::get_UnhideWhenUsed](./get_unhidewhenused/) için ayarlayıcı. |
| static [Type](./type/)() |  |

## Örnekler



Özel bir stilin nasıl oluşturulup uygulanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Stili otomatik olarak yeniden tanımlar.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgeden bir stili, belge oluşturucunun oluşturduğu paragrafa uygular.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Özel stilimizi belgenin stil koleksiyonundan kaldırın.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Kaldırılan bir stil kullanan tüm metinler varsayılan biçimlendirmeye geri döner.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```


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
