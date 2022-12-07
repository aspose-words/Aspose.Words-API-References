---
title: StyleCollection
second_title: Aspose.Words for C++ API Reference
description: A collection of Style objects that represent both the built-in and user-defined styles in a document. To learn more, visit the  documentation article.
type: docs
weight: 833
url: /cpp/aspose.words/stylecollection/
---
## StyleCollection class


A collection of [Style](../style/) objects that represent both the built-in and user-defined styles in a document. To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/) documentation article.

```cpp
class StyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Style>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(Aspose::Words::StyleType, const System::String\&) | Creates a new user defined style and adds it the collection. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Copies a style into this collection. |
| [ClearQuickStyleGallery](./clearquickstylegallery/)() | Removes all styles from the Quick [Style](../style/) Gallery panel. |
| [get_Count](./get_count/)() | Gets the number of styles in the collection. |
| [get_DefaultFont](./get_defaultfont/)() | Gets document default text formatting. |
| [get_DefaultParagraphFormat](./get_defaultparagraphformat/)() | Gets document default paragraph formatting. |
| [get_Document](./get_document/)() const | Gets the owner document. |
| [GetEnumerator](./getenumerator/)() override | Gets an enumerator object that will enumerate styles in the alphabetical order of their names. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Gets a style by name or alias. |
| [idx_get](./idx_get/)(Aspose::Words::StyleIdentifier) | Gets a built-in style by its locale independent identifier. |
| [idx_get](./idx_get/)(int32_t) | Gets a style by index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Examples



Shows how to create and use a paragraph style with list formatting. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a custom paragraph style.
SharedPtr<Style> style = doc->get_Styles()->Add(StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Create a list and make sure the paragraphs that use this style will use this list.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Change the document builder's style to one that has no list formatting and write another paragraph.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(ArtifactsDir + u"Styles.ParagraphStyleBulletedList.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
