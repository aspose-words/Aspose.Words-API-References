---
title: "Aspose::Words::DocumentBase::get_Styles método"
linktitle: "get_Styles"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBase::get_Styles. Devuelve una colección de estilos definidos en el documento en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/documentbase/get_styles/
---
## DocumentBase::get_Styles method


Devuelve una colección de estilos definidos en el documento.

```cpp
System::SharedPtr<Aspose::Words::StyleCollection> Aspose::Words::DocumentBase::get_Styles() const
```

## Observaciones


Para obtener más información, consulte la descripción de la clase [StyleCollection](../../stylecollection/).

## Ejemplos



Muestra cómo acceder a la colección de estilos de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Enumere y liste todos los estilos que contiene por defecto un documento creado con Aspose.Words.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> stylesEnum = doc->get_Styles()->GetEnumerator();
    while (stylesEnum->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Style> curStyle = stylesEnum->get_Current();
        std::cout << System::String::Format(u"Style name:\t\"{0}\", of type \"{1}\"", curStyle->get_Name(), curStyle->get_Type()) << std::endl;
        std::cout << System::String::Format(u"\tSubsequent style:\t{0}", curStyle->get_NextParagraphStyleName()) << std::endl;
        std::cout << System::String::Format(u"\tIs heading:\t\t\t{0}", curStyle->get_IsHeading()) << std::endl;
        std::cout << System::String::Format(u"\tIs QuickStyle:\t\t{0}", curStyle->get_IsQuickStyle()) << std::endl;

        ASPOSE_ASSERT_EQ(doc, curStyle->get_Document());
    }
}
```


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

* Class [StyleCollection](../../stylecollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
