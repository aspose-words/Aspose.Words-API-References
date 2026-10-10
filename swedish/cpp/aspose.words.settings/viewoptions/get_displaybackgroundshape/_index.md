---
title: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape‑metod"
linktitle: "get_DisplayBackgroundShape"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape‑metod. Styr visning av bakgrundsformen i utskriftslayout‑vyn i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.settings/viewoptions/get_displaybackgroundshape/
---
## ViewOptions::get_DisplayBackgroundShape method


Styr visning av bakgrundsformen i utskriftslayoutvy.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape() const
```


## Exempel



Visar hur man döljer/visar dokumentbakgrundsbilder i visningsalternativ.
```cpp
// Använd en HTML-sträng för att skapa ett nytt dokument med en enfärgad bakgrund.
const System::String html = u"<html>\r\n                <body style='background-color: blue'>\r\n                    <p>Hello world!</p>\r\n                </body>\r\n            </html>";

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_Unicode()->GetBytes(html)));

// Källan för dokumentet har en enfärgad bakgrund,
// vars närvaro kommer att sätta flaggan "DisplayBackgroundShape" till "true".
ASSERT_TRUE(doc->get_ViewOptions()->get_DisplayBackgroundShape());

// Behåll "DisplayBackgroundShape" som "true" för att låta dokumentet visa bakgrundsfärgen.
// Detta kan påverka vissa textfärger för att förbättra synligheten.
// Sätt "DisplayBackgroundShape" till "false" för att inte visa bakgrundsfärgen.
doc->get_ViewOptions()->set_DisplayBackgroundShape(displayBackgroundShape);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayBackgroundShape.docx");
```

## Se även

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
