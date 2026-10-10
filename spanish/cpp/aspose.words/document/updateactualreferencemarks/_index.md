---
title: "Aspose::Words::Document::UpdateActualReferenceMarks método"
linktitle: "UpdateActualReferenceMarks"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::UpdateActualReferenceMarks método. Actualiza la propiedad ActualReferenceMark de todas las notas al pie y notas finales en el documento en C++."
type: docs
weight: 95500
url: /es/cpp/aspose.words/document/updateactualreferencemarks/
---
## Document::UpdateActualReferenceMarks method


Actualiza la propiedad [ActualReferenceMark](../../../aspose.words.notes/footnote/get_actualreferencemark/) de todas las notas al pie y notas finales en el documento.

```cpp
void Aspose::Words::Document::UpdateActualReferenceMarks()
```


## Ejemplos



Muestra cómo obtener la marca de referencia real de la nota al pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
