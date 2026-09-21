---
title: "Aspose::Words::Lists::ListCollection::AddSingleLevelList metod"
linktitle: "AddSingleLevelList"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListCollection::AddSingleLevelList metod. Skapar en ny enkelnivålista baserad på den fördefinierade mallen och lägger till den i listsamlingen i dokumentet i C++."
type: docs
weight: 3500
url: /sv/cpp/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection::AddSingleLevelList method


Skapar en ny enkelnivålista baserad på den fördefinierade mallen och lägger till den i listsamlingen i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddSingleLevelList(Aspose::Words::Lists::ListTemplate listTemplate)
```


## Exempel



Visar hur man skapar en ny enkelnivålista baserad på den fördefinierade mallen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Lists::ListCollection> listCollection = doc->get_Lists();

// Skapar den punktlistade listan från BulletCircle-mallen.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Skriver den punktlistade listan till det resulterande dokumentet.
builder->Writeln(u"Bulleted list starts below:");
builder->get_ListFormat()->set_List(bulletedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Skapar den numrerade listan från NumberUppercaseLetterDot-mallen.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::NumberUppercaseLetterDot);

// Skriver den numrerade listan till det resulterande dokumentet.
builder->Writeln(u"Numbered list starts below:");
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Save(get_ArtifactsDir() + u"Lists.AddSingleLevelList.docx");
```

## Se även

* Class [List](../../list/)
* Enum [ListTemplate](../../listtemplate/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
