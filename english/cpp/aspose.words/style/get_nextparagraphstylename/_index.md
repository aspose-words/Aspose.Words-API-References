---
title: Aspose::Words::Style::get_NextParagraphStyleName method
linktitle: get_NextParagraphStyleName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::get_NextParagraphStyleName method. Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words/style/get_nextparagraphstylename/
---
## Style::get_NextParagraphStyleName method


Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style.

```cpp
System::String Aspose::Words::Style::get_NextParagraphStyleName()
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

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
