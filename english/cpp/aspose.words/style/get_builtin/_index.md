---
title: get_BuiltIn
second_title: Aspose.Words for C++ API Reference
description: True if this style is one of the built-in styles in MS Word.
type: docs
weight: 66
url: /cpp/aspose.words/style/get_builtin/
---
## Style::get_BuiltIn method


True if this style is one of the built-in styles in MS Word.

```cpp
bool Aspose::Words::Style::get_BuiltIn()
```


## Examples



Shows how to differentiate custom styles from built-in styles. 
```cpp
auto doc = MakeObject<Document>();

// When we create a document using Microsoft Word, or programmatically using Aspose.Words,
// the document will come with a collection of styles to apply to its text to modify its appearance.
// We can access these built-in styles via the document's "Styles" collection.
// These styles will all have the "BuiltIn" flag set to "true".
SharedPtr<Style> style = doc->get_Styles()->idx_get(u"Emphasis");

ASSERT_TRUE(style->get_BuiltIn());

// Create a custom style and add it to the collection.
// Custom styles such as this will have the "BuiltIn" flag set to "false".
style = doc->get_Styles()->Add(StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
style->get_Font()->set_Name(u"Courier New");

ASSERT_FALSE(style->get_BuiltIn());
```

## See Also

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
