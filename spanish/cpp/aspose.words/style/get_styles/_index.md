---
title: "Aspose::Words::Style::get_Styles método"
linktitle: "get_Styles"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Style::get_Styles método. Obtiene la colección de estilos a los que pertenece este estilo en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words/style/get_styles/
---
## Style::get_Styles method


Obtiene la colección de estilos a la que pertenece este estilo.

```cpp
System::SharedPtr<Aspose::Words::StyleCollection> Aspose::Words::Style::get_Styles() const
```


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

## Ver también

* Class [StyleCollection](../../stylecollection/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
