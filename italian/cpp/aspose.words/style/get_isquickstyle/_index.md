---
title: "Metodo Aspose::Words::Style::get_IsQuickStyle"
linktitle: "get_IsQuickStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Style::get_IsQuickStyle. Specifica se questo stile è mostrato nella galleria Quick Style all'interno dell'interfaccia di MS Word in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/style/get_isquickstyle/
---
## Style::get_IsQuickStyle method


Specifica se questo stile è mostrato nella galleria Quick [Style](../) all'interno dell'interfaccia di MS Word.

```cpp
bool Aspose::Words::Style::get_IsQuickStyle() const
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

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
