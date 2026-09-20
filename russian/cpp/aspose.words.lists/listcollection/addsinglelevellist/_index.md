---
title: "Aspose::Words::Lists::ListCollection::AddSingleLevelList метод"
linktitle: "AddSingleLevelList"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::ListCollection::AddSingleLevelList метод. Создаёт новый одноуровневый список на основе предопределённого шаблона и добавляет его в коллекцию списков в документе в C++."
type: docs
weight: 3500
url: /ru/cpp/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection::AddSingleLevelList method


Создаёт новый одноуровневый список на основе предопределённого шаблона и добавляет его в коллекцию списков в документе.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddSingleLevelList(Aspose::Words::Lists::ListTemplate listTemplate)
```


## Примеры



Показывает, как создать новый одноуровневый список на основе предопределённого шаблона.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Lists::ListCollection> listCollection = doc->get_Lists();

// Создаёт маркированный список из шаблона BulletCircle.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Записывает маркированный список в полученный документ.
builder->Writeln(u"Bulleted list starts below:");
builder->get_ListFormat()->set_List(bulletedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Создаёт нумерованный список из шаблона NumberUppercaseLetterDot.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::NumberUppercaseLetterDot);

// Записывает нумерованный список в результирующий документ.
builder->Writeln(u"Numbered list starts below:");
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Save(get_ArtifactsDir() + u"Lists.AddSingleLevelList.docx");
```

## См. также

* Class [List](../../list/)
* Enum [ListTemplate](../../listtemplate/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
