---
title: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method"
linktitle: "get_DisplayBackgroundShape"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape method. Controlla la visualizzazione della forma di sfondo nella visualizzazione di layout di stampa in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.settings/viewoptions/get_displaybackgroundshape/
---
## ViewOptions::get_DisplayBackgroundShape method


Controlla la visualizzazione della forma di sfondo nella visualizzazione layout di stampa.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape() const
```


## Esempi



Mostra come nascondere/visualizzare le immagini di sfondo del documento nelle opzioni di visualizzazione.
```cpp
// Usa una stringa HTML per creare un nuovo documento con un colore di sfondo uniforme.
const System::String html = u"<html>\r\n                <body style='background-color: blue'>\r\n                    <p>Hello world!</p>\r\n                </body>\r\n            </html>";

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_Unicode()->GetBytes(html)));

// La sorgente del documento ha uno sfondo di colore uniforme,
// la cui presenza imposterà il flag "DisplayBackgroundShape" su "true".
ASSERT_TRUE(doc->get_ViewOptions()->get_DisplayBackgroundShape());

// Mantieni "DisplayBackgroundShape" su "true" per fare in modo che il documento visualizzi il colore di sfondo.
// Ciò può influire su alcuni colori del testo per migliorare la visibilità.
// Imposta "DisplayBackgroundShape" su "false" per non visualizzare il colore di sfondo.
doc->get_ViewOptions()->set_DisplayBackgroundShape(displayBackgroundShape);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayBackgroundShape.docx");
```

## Vedi anche

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
