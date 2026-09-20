---
title: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade método"
linktitle: "get_ForeTintAndShade"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade método. Obtiene o establece un valor double que aclara o oscurece el color de primer plano en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.drawing/fill/get_foretintandshade/
---
## Fill::get_ForeTintAndShade method


Obtiene o establece un valor double que aclara o oscurece el color de primer plano.

```cpp
double Aspose::Words::Drawing::Fill::get_ForeTintAndShade()
```

## Observaciones


Los valores permitidos están en el rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad.

Cero (0) es neutral.

## Ejemplos



Muestra cómo gestionar el aclarado y oscurecimiento del color de fuente del primer plano.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::Drawing::Fill> textFill = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Fill();
textFill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
if (textFill->get_ForeTintAndShade() == 0)
{
    textFill->set_ForeTintAndShade(0.5);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillTintAndShade.docx");
```

## Ver también

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
