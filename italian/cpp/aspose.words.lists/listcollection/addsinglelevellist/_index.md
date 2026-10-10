---
title: "Aspose::Words::Lists::ListCollection::AddSingleLevelList metodo"
linktitle: "AddSingleLevelList"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Lists::ListCollection::AddSingleLevelList metodo. Crea una nuova lista a singolo livello basata sul modello predefinito e la aggiunge alla collezione di liste nel documento in C++."
type: docs
weight: 3500
url: /it/cpp/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection::AddSingleLevelList method


Crea un nuovo elenco a livello singolo basato sul modello predefinito e lo aggiunge alla collezione di elenchi nel documento.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddSingleLevelList(Aspose::Words::Lists::ListTemplate listTemplate)
```


## Esempi



Mostra come creare una nuova lista a singolo livello basata sul modello predefinito.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Lists::ListCollection> listCollection = doc->get_Lists();

// Crea l'elenco puntato dal modello BulletCircle.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Scrive l'elenco puntato nel documento risultante.
builder->Writeln(u"Bulleted list starts below:");
builder->get_ListFormat()->set_List(bulletedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Crea l'elenco numerato dal modello NumberUppercaseLetterDot.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::NumberUppercaseLetterDot);

// Scrive l'elenco numerato nel documento risultante.
builder->Writeln(u"Numbered list starts below:");
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Save(get_ArtifactsDir() + u"Lists.AddSingleLevelList.docx");
```

## Vedi anche

* Class [List](../../list/)
* Enum [ListTemplate](../../listtemplate/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
