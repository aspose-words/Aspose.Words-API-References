---
title: "Aspose::Words::Lists::ListCollection::AddSingleLevelList método"
linktitle: "AddSingleLevelList"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListCollection::AddSingleLevelList método. Crea una nueva lista de un solo nivel basada en la plantilla predefinida y la agrega a la colección de listas en el documento en C++."
type: docs
weight: 3500
url: /es/cpp/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection::AddSingleLevelList method


Crea una nueva lista de un solo nivel basada en la plantilla predefinida y la agrega a la colección de listas del documento.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddSingleLevelList(Aspose::Words::Lists::ListTemplate listTemplate)
```


## Ejemplos



Muestra cómo crear una nueva lista de un solo nivel basada en la plantilla predefinida.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Lists::ListCollection> listCollection = doc->get_Lists();

// Crea la lista con viñetas a partir de la plantilla BulletCircle.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Escribe la lista con viñetas en el documento resultante.
builder->Writeln(u"Bulleted list starts below:");
builder->get_ListFormat()->set_List(bulletedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Crea la lista numerada a partir de la plantilla NumberUppercaseLetterDot.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = listCollection->AddSingleLevelList(Aspose::Words::Lists::ListTemplate::NumberUppercaseLetterDot);

// Escribe la lista numerada en el documento resultante.
builder->Writeln(u"Numbered list starts below:");
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Save(get_ArtifactsDir() + u"Lists.AddSingleLevelList.docx");
```

## Ver también

* Class [List](../../list/)
* Enum [ListTemplate](../../listtemplate/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
