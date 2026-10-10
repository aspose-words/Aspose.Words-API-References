---
title: "Método Aspose::Words::PageSetup::get_ChapterPageSeparator"
linktitle: "get_ChapterPageSeparator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PageSetup::get_ChapterPageSeparator. Obtiene o establece el carácter separador que aparece entre el número de capítulo y el número de página en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words/pagesetup/get_chapterpageseparator/
---
## PageSetup::get_ChapterPageSeparator method


Obtiene o establece el carácter separador que aparece entre el número de capítulo y el número de página.

```cpp
Aspose::Words::ChapterPageSeparator Aspose::Words::PageSetup::get_ChapterPageSeparator()
```

## Observaciones


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

* Enum [ChapterPageSeparator](../../chapterpageseparator/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
