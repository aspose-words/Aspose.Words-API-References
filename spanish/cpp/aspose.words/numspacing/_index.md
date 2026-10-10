---
title: "Aspose::Words::NumSpacing enum"
linktitle: "NumSpacing"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::NumSpacing enum. Especifica los valores posibles en los que el espaciado de los numerales puede mostrarse en C++."
type: docs
weight: 103500
url: /es/cpp/aspose.words/numspacing/
---
## NumSpacing enum


Especifica los valores posibles en los que se puede mostrar el espaciado de los numerales.

```cpp
enum class NumSpacing
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Predeterminado | 0 | Especifica que los numerales se muestran en la forma predeterminada de la fuente. |
| Proporcional | 1 | Especifica que las formas de los numerales diseñadas como espaciado proporcional se muestran si la fuente lo soporta. |
| Tabular | 2 | Especifica que las formas de los numerales diseñadas como tabulares se muestren si la fuente lo admite. |


## Ejemplos



Muestra cómo establecer el tipo de espaciado del numeral.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Este efecto solo es compatible con versiones más recientes de MS Word.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
