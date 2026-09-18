---
title: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape Methode"
linktitle: "get_DisplayBackgroundShape"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape Methode. Steuert die Anzeige der Hintergrundform in der Drucklayout-Ansicht in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.settings/viewoptions/get_displaybackgroundshape/
---
## ViewOptions::get_DisplayBackgroundShape method


Steuert die Anzeige der Hintergrundform in der Drucklayout-Ansicht.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape() const
```


## Beispiele



Zeigt, wie man Dokument-Hintergrundbilder in den Ansichtoptionen ausblendet/anzeigt.
```cpp
// Verwenden Sie einen HTML-String, um ein neues Dokument mit einer einfarbigen Hintergrundfarbe zu erstellen.
const System::String html = u"<html>\r\n                <body style='background-color: blue'>\r\n                    <p>Hello world!</p>\r\n                </body>\r\n            </html>";

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_Unicode()->GetBytes(html)));

// Die Quelle für das Dokument hat einen einfarbigen Hintergrund,
// dessen Vorhandensein wird das Flag "DisplayBackgroundShape" auf "true" setzen.
ASSERT_TRUE(doc->get_ViewOptions()->get_DisplayBackgroundShape());

// Behalten Sie das "DisplayBackgroundShape" auf "true", damit das Dokument die Hintergrundfarbe anzeigt.
// Dies kann einige Textfarben beeinflussen, um die Sichtbarkeit zu verbessern.
// Setzen Sie das "DisplayBackgroundShape" auf "false", um die Hintergrundfarbe nicht anzuzeigen.
doc->get_ViewOptions()->set_DisplayBackgroundShape(displayBackgroundShape);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayBackgroundShape.docx");
```

## Siehe auch

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
