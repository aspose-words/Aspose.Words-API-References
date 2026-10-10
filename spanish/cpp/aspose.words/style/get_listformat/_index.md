---
title: "Aspose::Words::Style::get_ListFormat método"
linktitle: "get_ListFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Style::get_ListFormat método. Proporciona acceso a las propiedades de formato de lista de un estilo de párrafo en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words/style/get_listformat/
---
## Style::get_ListFormat method


Proporciona acceso a las propiedades de formato de lista de un estilo de párrafo.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListFormat> Aspose::Words::Style::get_ListFormat()
```

## Observaciones


Esta propiedad solo es válida para estilos de párrafo. Para otros tipos de estilo esta propiedad devuelve **null**.

## Ejemplos



Muestra cómo crear y usar un estilo de párrafo con formato de lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un estilo de párrafo personalizado.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Crea una lista y asegura que los párrafos que usan este estilo utilicen esta lista.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Aplica el estilo de párrafo al párrafo actual del generador de documentos y luego agrega algo de texto.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Cambie el estilo del document builder a uno que no tenga formato de lista y escriba otro párrafo.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Ver también

* Class [ListFormat](../../../aspose.words.lists/listformat/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
