---
title: "Aspose::Words::Section::Clone método"
linktitle: "Clonar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Section::Clone método. Crea un duplicado de esta sección en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/section/clone/
---
## Section::Clone method


Crea un duplicado de esta sección.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Section::Clone()
```


## Ejemplos



Muestra cómo agregar y eliminar secciones en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Elimine la primera sección del documento.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Añada una copia de lo que ahora es la primera sección al final del documento.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Ver también

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
