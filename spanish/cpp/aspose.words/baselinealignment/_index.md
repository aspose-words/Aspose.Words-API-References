---
title: "Aspose::Words::BaselineAlignment enum"
linktitle: "BaselineAlignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BaselineAlignment enum. Especifica la posición vertical de las fuentes en una línea en C++."
type: docs
weight: 80500
url: /es/cpp/aspose.words/baselinealignment/
---
## BaselineAlignment enum


Especifica la posición vertical de las fuentes en una línea.

```cpp
enum class BaselineAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Superior | 0 | Se alinea a lo largo de la parte superior de cada fuente. |
| Centro | 1 | Se alinea a los puntos centrales de cada fuente. |
| Línea base | 2 | Se alinea a la línea base del párrafo. |
| Inferior | 3 | Se alinea a la parte inferior de cada fuente. |
| Auto | 4 | La línea base se ajusta automáticamente. |


## Ejemplos



Muestra cómo establecer la posición vertical de las fuentes en una línea.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == Aspose::Words::BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(Aspose::Words::BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
