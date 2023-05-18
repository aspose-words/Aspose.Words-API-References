---
title: Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces method
linktitle: get_DetectNumberingWithWhitespaces
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces method. Allows to specify how numbered list items are recognized when document is imported from plain text format. The default value is true in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.loading/txtloadoptions/get_detectnumberingwithwhitespaces/
---
## TxtLoadOptions::get_DetectNumberingWithWhitespaces method


Allows to specify how numbered list items are recognized when document is imported from plain text format. The default value is **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces() const
```

## Remarks


If this option is set to **false**, lists recognition algorithm detects list paragraphs, when list numbers ends with either dot, right bracket or bullet symbols (such as "•", "*", "-" or "o").

If this option is set to **true**, whitespaces are also used as list number delimiters: list recognition algorithm for Arabic style numbering (1., 1.1.2.) uses both whitespaces and dot (".") symbols.

## Examples



Shows how to detect lists when loading plaintext documents. 
```cpp
// Create a plaintext document in a string with four separate parts that we may interpret as lists,
// with different delimiters. Upon loading the plaintext document into a "Document" object,
// Aspose.Words will always detect the first three lists and will add a "List" object
// for each to the document's "Lists" property.
const String textDoc = String(u"Full stop delimiters:\n") + u"1. First list item 1\n" + u"2. First list item 2\n" + u"3. First list item 3\n\n" +
                       u"Right bracket delimiters:\n" + u"1) Second list item 1\n" + u"2) Second list item 2\n" + u"3) Second list item 3\n\n" +
                       u"Bullet delimiters:\n" + u"• Third list item 1\n" + u"• Third list item 2\n" + u"• Third list item 3\n\n" +
                       u"Whitespace delimiters:\n" + u"1 Fourth list item 1\n" + u"2 Fourth list item 2\n" + u"3 Fourth list item 3";

// Create a "TxtLoadOptions" object, which we can pass to a document's constructor
// to modify how we load a plaintext document.
auto loadOptions = MakeObject<TxtLoadOptions>();

// Set the "DetectNumberingWithWhitespaces" property to "true" to detect numbered items
// with whitespace delimiters, such as the fourth list in our document, as lists.
// This may also falsely detect paragraphs that begin with numbers as lists.
// Set the "DetectNumberingWithWhitespaces" property to "false"
// to not create lists from numbered items with whitespace delimiters.
loadOptions->set_DetectNumberingWithWhitespaces(detectNumberingWithWhitespaces);

auto doc = MakeObject<Document>(MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    ASSERT_EQ(4, doc->get_Lists()->get_Count());
    ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(
        [](SharedPtr<Node> p) { return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Paragraph>(p))->get_IsListItem(); }));
}
else
{
    ASSERT_EQ(3, doc->get_Lists()->get_Count());
    ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(
        [](SharedPtr<Node> p) { return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Paragraph>(p))->get_IsListItem(); }));
}
```

## See Also

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
