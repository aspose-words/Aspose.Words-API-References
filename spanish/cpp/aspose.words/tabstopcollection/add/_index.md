---
title: "Método Aspose::Words::TabStopCollection::Add"
linktitle: "Add"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::TabStopCollection::Add. Añade o reemplaza una tabulación en la colección en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/tabstopcollection/add/
---
## TabStopCollection::Add(const System::SharedPtr\<Aspose::Words::TabStop\>\&) method


Agrega o reemplaza una tabulación en la colección.

```cpp
void Aspose::Words::TabStopCollection::Add(const System::SharedPtr<Aspose::Words::TabStop> &tabStop)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tabStop | const System::SharedPtr\<Aspose::Words::TabStop\>\& | Un objeto tabStop para añadir. |
## Observaciones


Si ya existe una tabulación en la posición especificada, se reemplaza.

## Ejemplos



Muestra cómo añadir tabulaciones personalizadas a un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// A continuación se presentan dos formas de añadir tabulaciones a la colección de tabulaciones de un párrafo mediante la propiedad "ParagraphFormat".
// 1 -  Crea un objeto "TabStop" y, a continuación, añádelo a la colección:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Pasa los valores de las propiedades de una nueva tabulación al método "Add":
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Añade tabulaciones a 5 cm en todos los párrafos.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Cada carácter "tab" lleva el cursor del constructor a la ubicación de la siguiente tabulación.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Ver también

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStopCollection::Add(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) method


Agrega o reemplaza una tabulación en la colección.

```cpp
void Aspose::Words::TabStopCollection::Add(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| posición | double | Una posición (en puntos) donde añadir la tabulación. |
| alignment | Aspose::Words::TabAlignment | Un valor [TabAlignment](../../tabalignment/) que especifica la alineación del texto en la tabulación. |
| leader | Aspose::Words::TabLeader | Un valor [TabLeader](../../tableader/) que especifica el tipo de línea guía mostrada bajo el carácter de tabulación. |
## Observaciones


Si ya existe una tabulación en la posición especificada, se reemplaza.

## Ejemplos



Muestra cómo añadir tabulaciones personalizadas a un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// A continuación se presentan dos formas de añadir tabulaciones a la colección de tabulaciones de un párrafo mediante la propiedad "ParagraphFormat".
// 1 -  Crea un objeto "TabStop" y, a continuación, añádelo a la colección:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Pasa los valores de las propiedades de una nueva tabulación al método "Add":
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Añade tabulaciones a 5 cm en todos los párrafos.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Cada carácter "tab" lleva el cursor del constructor a la ubicación de la siguiente tabulación.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Ver también

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
