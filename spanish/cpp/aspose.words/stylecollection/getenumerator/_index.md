---
title: "Aspose::Words::StyleCollection::GetEnumerator método"
linktitle: "GetEnumerator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::StyleCollection::GetEnumerator método. Obtiene un objeto enumerador que enumerará los estilos en orden alfabético de sus nombres en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/stylecollection/getenumerator/
---
## StyleCollection::GetEnumerator method


Obtiene un objeto enumerador que enumerará los estilos en orden alfabético de sus nombres.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> Aspose::Words::StyleCollection::GetEnumerator() override
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

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
