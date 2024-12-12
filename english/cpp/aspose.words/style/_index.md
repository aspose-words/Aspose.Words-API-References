---
title: Aspose::Words::Style class
linktitle: Style
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style class. Represents a single built-in or user-defined style. To learn more, visit the  documentation article in C++.'
type: docs
weight: 64000
url: /cpp/aspose.words/style/
---
## Style class


Represents a single built-in or user-defined style. To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/) documentation article.

```cpp
class Style : public Aspose::Words::IParaAttrSource,
              public Aspose::Words::IRunAttrSource
```

## Methods

| Method | Description |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared. |
| [get_Aliases](./get_aliases/)() | Gets all aliases of this style. If style has no aliases then empty array of string is returned. |
| [get_AutomaticallyUpdate](./get_automaticallyupdate/)() const | Specifies whether this style is automatically redefined based on the appropriate value. |
| [get_BaseStyleName](./get_basestylename/)() | Gets/sets the name of the style this style is based on. |
| [get_BuiltIn](./get_builtin/)() | True if this style is one of the built-in styles in MS Word. |
| [get_Document](./get_document/)() | Gets the owner document. |
| [get_Font](./get_font/)() | Gets the character formatting of the style. |
| [get_IsHeading](./get_isheading/)() | True when the style is one of the built-in Heading styles. |
| [get_IsQuickStyle](./get_isquickstyle/)() const | Specifies whether this style is shown in the Quick [Style](./) gallery inside MS Word UI. |
| [get_LinkedStyleName](./get_linkedstylename/)() | Gets/sets the name of the [Style](./) linked to this one. Returns empty string if no styles are linked. |
| [get_List](./get_list/)() | Gets the list that defines formatting of this list style. |
| [get_ListFormat](./get_listformat/)() | Provides access to the list formatting properties of a paragraph style. |
| [get_Locked](./get_locked/)() const | Specifies whether this style is locked. |
| [get_Name](./get_name/)() const | Gets or sets the name of the style. |
| [get_NextParagraphStyleName](./get_nextparagraphstylename/)() | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Gets the paragraph formatting of the style. |
| [get_Priority](./get_priority/)() const | Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane. |
| [get_SemiHidden](./get_semihidden/)() const | Gets/sets whether the style hides from the Styles gallery and from the Styles task pane. |
| [get_StyleIdentifier](./get_styleidentifier/)() const | Gets the locale independent style identifier for a built-in style. |
| [get_Styles](./get_styles/)() const | Gets the collection of styles this style belongs to. |
| [get_Type](./get_type/)() const | Gets the style type (paragraph or character). |
| [get_UnhideWhenUsed](./get_unhidewhenused/)() const | Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane. True when the used style should be shown in the Styles gallery. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Removes the specified style from the document. |
| [set_AutomaticallyUpdate](./set_automaticallyupdate/)(bool) | Setter for [Aspose::Words::Style::get_AutomaticallyUpdate](./get_automaticallyupdate/). |
| [set_BaseStyleName](./set_basestylename/)(const System::String\&) | Setter for [Aspose::Words::Style::get_BaseStyleName](./get_basestylename/). |
| [set_IsQuickStyle](./set_isquickstyle/)(bool) | Setter for [Aspose::Words::Style::get_IsQuickStyle](./get_isquickstyle/). |
| [set_LinkedStyleName](./set_linkedstylename/)(const System::String\&) | Setter for [Aspose::Words::Style::get_LinkedStyleName](./get_linkedstylename/). |
| [set_Locked](./set_locked/)(bool) | Specifies whether this style is locked. |
| [set_Name](./set_name/)(const System::String\&) | Setter for [Aspose::Words::Style::get_Name](./get_name/). |
| [set_NextParagraphStyleName](./set_nextparagraphstylename/)(const System::String\&) | Setter for [Aspose::Words::Style::get_NextParagraphStyleName](./get_nextparagraphstylename/). |
| [set_Priority](./set_priority/)(int32_t) | Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane. |
| [set_SemiHidden](./set_semihidden/)(bool) | Gets/sets whether the style hides from the Styles gallery and from the Styles task pane. |
| [set_UnhideWhenUsed](./set_unhidewhenused/)(bool) | Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane. True when the used style should be shown in the Styles gallery. |
| static [Type](./type/)() |  |

## Examples



Shows how to create and apply a custom style. 
```cpp
auto doc = MakeObject<Document>();

SharedPtr<Style> style = doc->get_Styles()->Add(StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());

auto builder = MakeObject<DocumentBuilder>(doc);

// Apply one of the styles from the document to the paragraph that the document builder is creating.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

SharedPtr<Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Remove our custom style from the document's styles collection.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Any text that used a removed style reverts to the default formatting.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any([](SharedPtr<Style> s) { return s->get_Name() == u"MyStyle"; }));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```


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
* Library [Aspose.Words for C++](../../)
