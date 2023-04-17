---
title: Aspose::Words::Font::get_StyleIdentifier method
linktitle: get_StyleIdentifier
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_StyleIdentifier method. Gets or sets the locale independent style identifier of the character style applied to this formatting in C++.'
type: docs
weight: 43000
url: /cpp/aspose.words/font/get_styleidentifier/
---
## Font::get_StyleIdentifier method


Gets or sets the locale independent style identifier of the character style applied to this formatting.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Font::get_StyleIdentifier()
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

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
