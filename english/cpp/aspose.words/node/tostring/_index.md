---
title: ToString
second_title: Aspose.Words for C++ API Reference
description: Exports the content of the node into a string in the specified format.
type: docs
weight: 222
url: /cpp/aspose.words/node/tostring/
---
## Node::ToString(Aspose::Words::SaveFormat) method


Exports the content of the node into a string in the specified format.

```cpp
System::String Aspose::Words::Node::ToString(Aspose::Words::SaveFormat saveFormat)
```


### ReturnValue

The content of the node in the specified format.

## Examples



Shows the difference between calling the GetText and ToString methods on a node. 
```cpp
auto doc = MakeObject<Document>();

auto builder = MakeObject<DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText will retrieve the visible text as well as field codes and special characters.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc->GetText());

// ToString will give us the document's appearance if saved to a passed save format.
ASSERT_EQ(u"«Field»\r\n", doc->ToString(SaveFormat::Text));
```


Shows how to extract the list labels of all paragraphs that are list items. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");
doc->UpdateListLabels();

SharedPtr<NodeCollection> paras = doc->GetChildNodes(NodeType::Paragraph, true);

// Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
// which start at three and ends at six.
for (auto paragraph : System::IterateOver(
         paras->LINQ_OfType<SharedPtr<Paragraph>>()->LINQ_Where([](SharedPtr<Paragraph> p) { return p->get_ListFormat()->get_IsListItem(); })))
{
    std::cout << "List item paragraph #" << paras->IndexOf(paragraph) << std::endl;

    // This is the text we get when getting when we output this node to text format.
    // This text output will omit list labels. Trim any paragraph formatting characters.
    String paragraphText = paragraph->ToString(SaveFormat::Text).Trim();
    std::cout << "\tExported Text: " << paragraphText << std::endl;

    SharedPtr<ListLabel> label = paragraph->get_ListLabel();

    // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
    // this will tell us what position it is on that level.
    std::cout << "\tNumerical Id: " << label->get_LabelValue() << std::endl;

    // Combine them together to include the list label with the text in the output.
    std::cout << "\tList label combined with text: " << label->get_LabelString() << " " << paragraphText << std::endl;
}
```


Exports the content of a node to String in HTML format. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

SharedPtr<Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// When we call the ToString method using the html SaveFormat overload,
// it converts the node's contents to their raw html representation.
ASSERT_EQ(String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") +
              u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>",
          node->ToString(SaveFormat::Html));

// We can also modify the result of this conversion using a SaveOptions object.
auto saveOptions = MakeObject<HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") +
              u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>",
          node->ToString(saveOptions));
```

## See Also

* Enum [SaveFormat](../../saveformat/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## Node::ToString(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Exports the content of the node into a string using the specified save options.

```cpp
System::String Aspose::Words::Node::ToString(const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Specifies the options that control how the node is saved. |

### ReturnValue

The content of the node in the specified format.

## Examples



Exports the content of a node to String in HTML format. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

SharedPtr<Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// When we call the ToString method using the html SaveFormat overload,
// it converts the node's contents to their raw html representation.
ASSERT_EQ(String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") +
              u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>",
          node->ToString(SaveFormat::Html));

// We can also modify the result of this conversion using a SaveOptions object.
auto saveOptions = MakeObject<HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") +
              u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>",
          node->ToString(saveOptions));
```

## See Also

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
