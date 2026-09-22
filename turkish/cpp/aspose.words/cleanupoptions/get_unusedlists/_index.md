---
title: "Aspose::Words::CleanupOptions::get_UnusedLists yöntemi"
linktitle: "get_UnusedLists"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CleanupOptions::get_UnusedLists yöntemi. Kullanılmayan liste ve liste tanımlarının belgelerden kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer C++'ta doğrudur."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/cleanupoptions/get_unusedlists/
---
## CleanupOptions::get_UnusedLists method


Belgeden kullanılmayan liste ve liste tanımlarının kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer **true**.

```cpp
bool Aspose::Words::CleanupOptions::get_UnusedLists() const
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

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
