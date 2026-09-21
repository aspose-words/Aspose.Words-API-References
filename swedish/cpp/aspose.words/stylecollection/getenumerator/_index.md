---
title: "Aspose::Words::StyleCollection::GetEnumerator‑metod"
linktitle: "GetEnumerator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::StyleCollection::GetEnumerator‑metod. Hämtar ett enumerator‑objekt som enumererar stilar i alfabetisk ordning efter deras namn i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/stylecollection/getenumerator/
---
## StyleCollection::GetEnumerator method


Hämtar ett enumerator-objekt som kommer att lista stilar i alfabetisk ordning efter deras namn.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> Aspose::Words::StyleCollection::GetEnumerator() override
```


## Exempel



Visar hur man får åtkomst till ett dokuments stilkollektion.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Enumerera och lista alla stilar som ett dokument skapat med Aspose.Words innehåller som standard.
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

## Se även

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
