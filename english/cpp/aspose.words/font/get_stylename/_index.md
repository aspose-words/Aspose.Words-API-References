---
title: get_StyleName
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of the character style applied to this formatting.
type: docs
weight: 547
url: /cpp/aspose.words/font/get_stylename/
---
## Font::get_StyleName method


Gets or sets the name of the character style applied to this formatting.

```cpp
System::String Aspose::Words::Font::get_StyleName()
```


## Examples



Shows how to change the style of existing text. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two ways of referencing styles.
// 1 -  Using the style name:
builder->get_Font()->set_StyleName(u"Emphasis");
builder->Writeln(u"Text originally in \"Emphasis\" style");

// 2 -  Using a built-in style identifier:
builder->get_Font()->set_StyleIdentifier(StyleIdentifier::IntenseEmphasis);
builder->Writeln(u"Text originally in \"Intense Emphasis\" style");

// Convert all uses of one style to another,
// using the above methods to reference old and new styles.
for (const auto& run : System::IterateOver(doc->GetChildNodes(NodeType::Run, true)->LINQ_OfType<SharedPtr<Run>>()))
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

doc->Save(ArtifactsDir + u"Font.ChangeStyle.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
