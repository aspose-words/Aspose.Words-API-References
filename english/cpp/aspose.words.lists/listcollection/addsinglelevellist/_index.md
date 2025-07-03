---
title: Aspose::Words::Lists::ListCollection::AddSingleLevelList method
linktitle: AddSingleLevelList
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListCollection::AddSingleLevelList method. Creates a new single level list based on the predefined template and adds it to the list collection in the document in C++.'
type: docs
weight: 3500
url: /cpp/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection::AddSingleLevelList method


Creates a new single level list based on the predefined template and adds it to the list collection in the document.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddSingleLevelList(Aspose::Words::Lists::ListTemplate listTemplate)
```


## Examples



Shows how to create a new single level list based on the predefined template. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Lists::ListCollection> listCollection = doc->get_Lists();

// Creates the bulleted list from BulletCircle template.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Writes the bulleted list to the resulting document.
builder->Writeln(u"Bulleted list starts below:");
builder->get_ListFormat()->set_List(bulletedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Creates the numbered list from NumberUppercaseLetterDot template.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::NumberUppercaseLetterDot);

// Writes the numbered list to the resulting document.
builder->Writeln(u"Numbered list starts below:");
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Save(get_ArtifactsDir() + u"Lists.AddSingleLevelList.docx");
```

## See Also

* Class [List](../../list/)
* Enum [ListTemplate](../../listtemplate/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
