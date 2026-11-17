---
title: Aspose::Words::Style::get_Name method
linktitle: get_Name
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::get_Name method. Gets or sets the name of the style in C++.'
type: docs
weight: 22595
url: /cpp/aspose.words/style/get_name/
---
## Style::get_Name method


Gets or sets the name of the style.

```cpp
System::String Aspose::Words::Style::get_Name() const
```

## Remarks


Can not be empty string.

If there already is a style with such name in the collection, then this style will override it. All affected nodes will reference new style.
## Examples


Shows how to access a document's style collection.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(doc->get_Styles()->get_Count(), 4);

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

        ASPOSE_ASSERT_EQ(curStyle->get_Document(), doc);
    }
}
```

Shows how to clone a document's style.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// The AddCopy method creates a copy of the specified style and
// automatically generates a new name for the style, such as "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Use the style's "Name" property to change the style's identifying name.
newStyle->set_Name(u"My Heading 1");

// Our document now has two identical looking styles with different names.
// Changing settings of one of the styles do not affect the other.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(newStyle->get_Name(), u"My Heading 1");
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Name(), u"Heading 1");

ASSERT_EQ(newStyle->get_Type(), doc->get_Styles()->idx_get(u"Heading 1")->get_Type());
ASSERT_EQ(newStyle->get_Font()->get_Name(), doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(newStyle->get_Font()->get_Size(), doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size());
ASPOSE_ASSERT_NE(newStyle->get_Font()->get_Color(), doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color());
```
## See Also

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
