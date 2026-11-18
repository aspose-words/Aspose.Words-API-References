---
title: Aspose::Words::Font::set_StyleIdentifier method
linktitle: set_StyleIdentifier
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_StyleIdentifier method. Sets the locale independent style identifier of the character style applied to this formatting in C++.'
type: docs
weight: 95000
url: /cpp/aspose.words/font/set_styleidentifier/
---
## Font::set_StyleIdentifier method


Sets the locale independent style identifier of the character style applied to this formatting.

```cpp
void Aspose::Words::Font::set_StyleIdentifier(Aspose::Words::StyleIdentifier value)
```

## Examples


Shows how to change the style of existing text.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Below are two ways of referencing styles.
// 1 -  Using the style name:
builder->get_Font()->set_StyleName(u"Emphasis");
builder->Writeln(u"Text originally in \"Emphasis\" style");

// 2 -  Using a built-in style identifier:
builder->get_Font()->set_StyleIdentifier(StyleIdentifier::IntenseEmphasis);
builder->Writeln(u"Text originally in \"Intense Emphasis\" style");

// Convert all uses of one style to another,
// using the above methods to reference old and new styles.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(NodeType::Run, true)))
{
    if (run->get_Font()->get_StyleName() == u"Emphasis")
    {
        run->get_Font()->set_StyleName(u"Strong");
    }

    if (run->get_Font()->get_StyleIdentifier() == StyleIdentifier::IntenseEmphasis)
    {
        run->get_Font()->set_StyleIdentifier(StyleIdentifier::Strong);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.ChangeStyle.docx");
```
## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
