---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign método"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign método. Especifica si los caracteres de barra invertida deben reemplazarse por signos de yen. El valor predeterminado es false en C++."
type: docs
weight: 5500
url: /es/cpp/aspose.words.saving/xamlflowsaveoptions/get_replacebackslashwithyensign/
---
## XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign method


Especifica si los caracteres de barra invertida deben reemplazarse por signos de yen. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## Ejemplos



Muestra cómo reemplazar los caracteres de barra invertida por signos de yen (Xaml).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// Por defecto, Aspose.Words imita el comportamiento de MS Word y no reemplaza los caracteres de barra invertida por signos de yen en
// documentos HTML generados. Sin embargo, versiones anteriores de Aspose.Words realizaban tales reemplazos en ciertos
// escenarios. Esta bandera habilita la compatibilidad hacia atrás con versiones anteriores de Aspose.Words.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XamlFlowSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

## Ver también

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
