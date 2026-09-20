---
title: "Constructor Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions"
linktitle: "RtfLoadOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor de Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions. Inicializa una nueva instancia de esta clase con valores predeterminados en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions::RtfLoadOptions constructor


Inicializa una nueva instancia de esta clase con valores predeterminados.

```cpp
Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions()
```


## Ejemplos



Muestra cómo detectar caracteres UTF-8 al cargar un documento RTF.
```cpp
// Cree un objeto "RtfLoadOptions" para modificar la forma en que cargamos un documento RTF.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// Establezca la propiedad "RecognizeUtf8Text" en "false" para asumir que el documento utiliza el conjunto de caracteres ISO 8859-1
// y carga cada carácter del documento.
// Establezca la propiedad "RecognizeUtf8Text" en "true" para analizar cualquier carácter de longitud variable que pueda aparecer en el texto.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## Ver también

* Class [RtfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
