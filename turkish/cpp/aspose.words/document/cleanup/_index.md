---
title: "Aspose::Words::Document::Cleanup yöntemi"
linktitle: "Cleanup"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::Cleanup yöntemi. C++'ta belgede kullanılmayan stilleri ve listeleri temizler."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/document/cleanup/
---
## Document::Cleanup() method


Belgeden kullanılmayan stilleri ve listeleri temizler.

```cpp
void Aspose::Words::Document::Cleanup()
```


## Örnekler



Bir belgede kullanılmayan özel stillerin nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// Yerleşik stillerle birleştirildiğinde, belgenin artık sekiz stili var.
// Bir özel stil, belgenin bir bölümüne uygulandığında "kullanılmış" sayılır,
// bu, eklediğimiz dört stilin şu anda kullanılmadığı anlamına gelir.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Önce bir özel karakter stili, ardından bir özel liste stili uygulayın. Böyle yapmak stilleri "kullanılmış" olarak işaretleyecektir.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Cleanup();

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// Özel bir stilin uygulandığı her düğümü kaldırmak, stili tekrar "kullanılmıyor" olarak işaretler.
// Onları kaldırmak için Cleanup yöntemini tekrar çalıştırın.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup();

ASSERT_EQ(4, doc->get_Styles()->get_Count());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Cleanup(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) method


Belirtilen [CleanupOptions](../../cleanupoptions/) doğrultusunda belgede kullanılmayan stilleri ve listeleri temizler.

```cpp
void Aspose::Words::Document::Cleanup(const System::SharedPtr<Aspose::Words::CleanupOptions> &options)
```


## Örnekler



Bir belgede tüm kullanılmayan özel stillerin nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// Yerleşik stillerle birleştirildiğinde, belgenin artık sekiz stili var.
// Belge içinde herhangi bir metin olduğu sürece özel bir stil "kullanıldı" olarak işaretlenir
// o stilde biçimlendirilir. Bu, eklediğimiz 4 stilin şu anda kullanılmadığı anlamına gelir.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Özel bir karakter stili uygulayın, ardından özel bir liste stili uygulayın. Bunu yapmak onları "kullanıldı" olarak işaretleyecektir.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

// Şimdi, bir kullanılmayan karakter stili ve bir kullanılmayan liste stili var.
// Cleanup() yöntemi, bir CleanupOptions nesnesiyle yapılandırıldığında, kullanılmayan stilleri hedef alabilir ve kaldırabilir.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_UnusedLists(true);
cleanupOptions->set_UnusedStyles(true);
cleanupOptions->set_UnusedBuiltinStyles(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Özel bir stilin uygulandığı her düğümü kaldırmak, stili tekrar "kullanılmıyor" olarak işaretler.
// Onları kaldırmak için Cleanup yöntemini yeniden çalıştırın.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup(cleanupOptions);

ASSERT_EQ(2, doc->get_Styles()->get_Count());
```

## Ayrıca Bakınız

* Class [CleanupOptions](../../cleanupoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
