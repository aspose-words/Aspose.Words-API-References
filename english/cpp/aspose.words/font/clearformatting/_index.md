---
title: Aspose::Words::Font::ClearFormatting method
linktitle: ClearFormatting
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::ClearFormatting method. Resets to default font formatting in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/font/clearformatting/
---
## Font::ClearFormatting method


Resets to default font formatting.

```cpp
void Aspose::Words::Font::ClearFormatting()
```

## Remarks


Removes all font formatting specified explicitly on the object from which [Font](../) was obtained so the font formatting will be inherited from the appropriate parent.

## Examples



Shows how to insert a hyperlink field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Insert a hyperlink and emphasize it with custom formatting.
// The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
doc->Save(ArtifactsDir + u"DocumentBuilder.InsertHyperlink.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
