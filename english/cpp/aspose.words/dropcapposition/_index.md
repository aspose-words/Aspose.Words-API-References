---
title: Aspose::Words::DropCapPosition enum
linktitle: DropCapPosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DropCapPosition enum. Specifies the position for a drop cap text in C++.'
type: docs
weight: 87000
url: /cpp/aspose.words/dropcapposition/
---
## DropCapPosition enum


Specifies the position for a drop cap text.

```cpp
enum class DropCapPosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | The paragraph does not have a drop cap. |
| Normal | 1 | The drop cap is positioned inside the text margin on the anchor paragraph. |
| Margin | 2 | The drop cap is positioned outside the text margin on the anchor paragraph. |


## Examples



Shows how to create a drop cap. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert one paragraph with a large letter that the text in the second and third paragraphs begins with.
builder->get_Font()->set_Size(54);
builder->Writeln(u"L");

builder->get_Font()->set_Size(18);
builder->Writeln(System::String(u"orem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder->Writeln(System::String(u"Ut enim ad minim veniam, quis nostrud exercitation ") + u"ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Currently, the second and third paragraphs will appear underneath the first.
// We can convert the first paragraph as a drop cap for the other paragraphs via its "ParagraphFormat" object.
// Set the "DropCapPosition" property to "DropCapPosition.Margin" to place the drop cap
// outside the left-hand side page margin if our text is left-to-right.
// Set the "DropCapPosition" property to "DropCapPosition.Normal" to place the drop cap within the page margins
// and to wrap the rest of the text around it.
// "DropCapPosition.None" is the default state for all paragraphs.
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_DropCapPosition(dropCapPosition);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.DropCap.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
