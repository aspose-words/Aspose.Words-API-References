---
title: "Aspose::Words::ChapterPageSeparator enum"
linktitle: "ChapterPageSeparator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ChapterPageSeparator enum. Define el carácter separador que aparece entre el capítulo y el número de página en C++."
type: docs
weight: 84000
url: /es/cpp/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enum


Define el carácter separador que aparece entre el número de capítulo y de página.

```cpp
enum class ChapterPageSeparator
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Guion | 0 | Dos puntos. |
| Punto | 1 | Un punto. |
| Dos puntos | 2 | Dos puntos. |
| Guion largo | 3 | Un guion enfatizado. |
| Guion medio | 4 | Un guion estándar. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
