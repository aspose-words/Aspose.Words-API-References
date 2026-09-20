---
title: "Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text método"
linktitle: "get_RecognizeUtf8Text"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text método. Cuando se establece en true, intentará detectar caracteres UTF8, los cuales se conservarán durante la importación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.loading/rtfloadoptions/get_recognizeutf8text/
---
## RtfLoadOptions::get_RecognizeUtf8Text method


Cuando se establece en **true**, intentará detectar caracteres UTF8, los cuales se conservarán durante la importación.

```cpp
bool Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text() const
```

## Observaciones


El valor predeterminado es **false**.

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
