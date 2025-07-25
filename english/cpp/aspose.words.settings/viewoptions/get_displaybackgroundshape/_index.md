---
title: Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method
linktitle: get_DisplayBackgroundShape
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method. Controls display of the background shape in print layout view in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.settings/viewoptions/get_displaybackgroundshape/
---
## ViewOptions::get_DisplayBackgroundShape method


Controls display of the background shape in print layout view.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape() const
```


## Examples



Shows how to hide/display document background images in view options. 
```cpp
// Use an HTML string to create a new document with a flat background color.
const System::String html = u"<html>\r\n                <body style='background-color: blue'>\r\n                    <p>Hello world!</p>\r\n                </body>\r\n            </html>";

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_Unicode()->GetBytes(html)));

// The source for the document has a flat color background,
// the presence of which will set the "DisplayBackgroundShape" flag to "true".
ASSERT_TRUE(doc->get_ViewOptions()->get_DisplayBackgroundShape());

// Keep the "DisplayBackgroundShape" as "true" to get the document to display the background color.
// This may affect some text colors to improve visibility.
// Set the "DisplayBackgroundShape" to "false" to not display the background color.
doc->get_ViewOptions()->set_DisplayBackgroundShape(displayBackgroundShape);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayBackgroundShape.docx");
```

## See Also

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
