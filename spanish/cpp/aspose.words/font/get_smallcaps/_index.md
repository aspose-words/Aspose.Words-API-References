---
title: "Aspose::Words::Font::get_SmallCaps método"
linktitle: "get_SmallCaps"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_SmallCaps método. Verdadero si la fuente está formateada como letras capitales pequeñas en C++."
type: docs
weight: 38000
url: /es/cpp/aspose.words/font/get_smallcaps/
---
## Font::get_SmallCaps method


True si la fuente está formateada como letras capitales pequeñas.

```cpp
bool Aspose::Words::Font::get_SmallCaps()
```


## Ejemplos



Muestra cómo formatear un fragmento para mostrar su contenido en mayúsculas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Hay dos formas de lograr que un fragmento muestre su texto en minúsculas en mayúsculas sin cambiar el contenido.
// 1 -  Establezca la bandera AllCaps para mostrar todos los caracteres en mayúsculas regulares:
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"all capitals");
run->get_Font()->set_AllCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

// 2 -  Establezca la bandera SmallCaps para mostrar todos los caracteres en mayúsculas pequeñas:
// Si un carácter está en minúscula, aparecerá en su forma mayúscula
// pero tendrá la misma altura que la minúscula (la altura x de la fuente).
// Los caracteres que estaban en mayúscula originalmente se verán iguales.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Small Capitals");
run->get_Font()->set_SmallCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.Caps.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
