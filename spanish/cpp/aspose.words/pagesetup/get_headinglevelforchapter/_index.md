---
title: "Aspose::Words::PageSetup::get_HeadingLevelForChapter método"
linktitle: "get_HeadingLevelForChapter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_HeadingLevelForChapter método. Obtiene o establece el estilo de nivel de encabezado que se aplica a los títulos de capítulo en el documento en C++."
type: docs
weight: 20000
url: /es/cpp/aspose.words/pagesetup/get_headinglevelforchapter/
---
## PageSetup::get_HeadingLevelForChapter method


Obtiene o establece el estilo de nivel de encabezado que se aplica a los títulos de los capítulos en el documento.

```cpp
int32_t Aspose::Words::PageSetup::get_HeadingLevelForChapter()
```

## Observaciones


Puede ser un número del 0 al 9. 0 significa que no hay número de capítulo si se aplica al número de página.

Antes de poder crear números de página que incluyan números de capítulo, los encabezados del documento deben tener aplicado un formato de esquema numerado.

## Ejemplos



Muestra cómo trabajar con capítulos de página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();

pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
pageSetup->set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator::Colon);
pageSetup->set_HeadingLevelForChapter(1);
```

## Ver también

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
