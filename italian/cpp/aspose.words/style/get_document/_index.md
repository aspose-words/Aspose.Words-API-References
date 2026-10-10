---
title: "Aspose::Words::Style::get_Document metodo"
linktitle: "get_Document"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Style::get_Document metodo. Restituisce il documento proprietario in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/style/get_document/
---
## Style::get_Document method


Restituisce il documento proprietario.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Style::get_Document()
```


## Esempi



Mostra come accedere alla raccolta di stili di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Elenca e visualizza tutti gli stili che un documento creato con Aspose.Words contiene per impostazione predefinita.
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

## Vedi anche

* Class [DocumentBase](../../documentbase/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
