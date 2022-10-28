---
title: get_Style
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the paragraph style applied to this formatting.
type: docs
weight: 430
url: /cpp/aspose.words/paragraphformat/get_style/
---
## ParagraphFormat.get_Style method


Gets or sets the paragraph style applied to this formatting.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::ParagraphFormat::get_Style()
```


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

