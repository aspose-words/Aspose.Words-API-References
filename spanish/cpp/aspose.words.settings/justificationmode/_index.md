---
title: "Aspose::Words::Settings::JustificationMode enum"
linktitle: "JustificationMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Settings::JustificationMode enum. Especifica el ajuste del espaciado de caracteres para un documento. El valor predeterminado es Expand en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.settings/justificationmode/
---
## JustificationMode enum


Especifica el ajuste del espaciado de caracteres para un documento. El valor predeterminado es **Expand**.

```cpp
enum class JustificationMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Expand | 0 | No comprimir el espaciado de caracteres. |
| Compress | 1 | Comprimir el espaciado de caracteres. |
| CompressKana | 2 | Comprimir, usando las reglas de los silabarios kana, Hiragana y Katakana. |


## Ejemplos



Muestra cómo gestionar el control del espaciado de caracteres.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## Ver también

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
