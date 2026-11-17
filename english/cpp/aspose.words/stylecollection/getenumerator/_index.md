---
title: Aspose::Words::StyleCollection::GetEnumerator method
linktitle: GetEnumerator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::StyleCollection::GetEnumerator method. Gets an enumerator object that will enumerate styles in the alphabetical order of their names in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words/stylecollection/getenumerator/
---
## StyleCollection::GetEnumerator method


Gets an enumerator object that will enumerate styles in the alphabetical order of their names.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> Aspose::Words::StyleCollection::GetEnumerator() override
```


## Examples



Shows how to access a document's style collection. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Enumerate and list all the styles that a document created using Aspose.Words contains by default.
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

## See Also

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
