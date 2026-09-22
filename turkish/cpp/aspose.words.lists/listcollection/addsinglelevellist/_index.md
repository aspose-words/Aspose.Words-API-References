---
title: "Aspose::Words::Lists::ListCollection::AddSingleLevelList metodu"
linktitle: "AddSingleLevelList"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListCollection::AddSingleLevelList metodu. Önceden tanımlı şablona dayalı yeni tek seviyeli bir liste oluşturur ve belge içindeki liste koleksiyonuna C++'ta ekler."
type: docs
weight: 3500
url: /tr/cpp/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection::AddSingleLevelList method


Önceden tanımlanmış şablona dayalı yeni tek seviyeli bir liste oluşturur ve belge içindeki liste koleksiyonuna ekler.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddSingleLevelList(Aspose::Words::Lists::ListTemplate listTemplate)
```


## Örnekler



Önceden tanımlı şablona dayalı yeni tek seviyeli bir listenin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Lists::ListCollection> listCollection = doc->get_Lists();

// BulletCircle şablonundan madde işaretli liste oluşturur.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Madde işaretli listeyi sonuç belgeye yazar.
builder->Writeln(u"Bulleted list starts below:");
builder->get_ListFormat()->set_List(bulletedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// NumberUppercaseLetterDot şablonundan numaralı liste oluşturur.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::NumberUppercaseLetterDot);

// Numaralı listeyi sonuç belgesine yazar.
builder->Writeln(u"Numbered list starts below:");
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Save(get_ArtifactsDir() + u"Lists.AddSingleLevelList.docx");
```

## Ayrıca Bakınız

* Class [List](../../list/)
* Enum [ListTemplate](../../listtemplate/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
