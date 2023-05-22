---
title: Aspose::Words::Font::get_Style method
linktitle: get_Style
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Style method. Gets or sets the character style applied to this formatting in C++.'
type: docs
weight: 42000
url: /cpp/aspose.words/font/get_style/
---
## Font::get_Style method


Gets or sets the character style applied to this formatting.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Font::get_Style()
```


## Examples



Applies a double underline to all runs in a document that are formatted with custom character styles. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a custom style and apply it to text created using a document builder.
SharedPtr<Style> style = doc->get_Styles()->Add(StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Red());
style->get_Font()->set_Name(u"Courier New");

builder->get_Font()->set_StyleName(u"MyStyle");
builder->Write(u"This text is in a custom style.");

// Iterate over every run and add a double underline to every custom style.
for (const auto& run : System::IterateOver(doc->GetChildNodes(NodeType::Run, true)->LINQ_OfType<SharedPtr<Run>>()))
{
    SharedPtr<Style> charStyle = run->get_Font()->get_Style();

    if (!charStyle->get_BuiltIn())
    {
        run->get_Font()->set_Underline(Underline::Double);
    }
}

doc->Save(ArtifactsDir + u"Font.Style.docx");
```

## See Also

* Class [Style](../../style/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
