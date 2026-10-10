---
title: "Aspose::Words::Lists::ListCollection::AddSingleLevelList Methode"
linktitle: "AddSingleLevelList"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListCollection::AddSingleLevelList Methode. Erstellt eine neue einstufige Liste basierend auf der vordefinierten Vorlage und fügt sie der Listensammlung im Dokument in C++ hinzu."
type: docs
weight: 3500
url: /de/cpp/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection::AddSingleLevelList method


Erstellt eine neue einstufige Liste basierend auf der vordefinierten Vorlage und fügt sie der Listensammlung im Dokument hinzu.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddSingleLevelList(Aspose::Words::Lists::ListTemplate listTemplate)
```


## Beispiele



Zeigt, wie man eine neue einstufige Liste basierend auf der vordefinierten Vorlage erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Lists::ListCollection> listCollection = doc->get_Lists();

// Erstellt die Aufzählungsliste aus der BulletCircle-Vorlage.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Schreibt die Aufzählungsliste in das resultierende Dokument.
builder->Writeln(u"Bulleted list starts below:");
builder->get_ListFormat()->set_List(bulletedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Erstellt die nummerierte Liste aus der Vorlage NumberUppercaseLetterDot.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::NumberUppercaseLetterDot);

// Schreibt die nummerierte Liste in das resultierende Dokument.
builder->Writeln(u"Numbered list starts below:");
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Save(get_ArtifactsDir() + u"Lists.AddSingleLevelList.docx");
```

## Siehe auch

* Class [List](../../list/)
* Enum [ListTemplate](../../listtemplate/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
