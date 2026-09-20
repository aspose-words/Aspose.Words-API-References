---
title: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat método"
linktitle: "get_IncludeTextboxesFootnotesEndnotesInStat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat método. Especifica si se deben incluir cuadros de texto, notas al pie y notas finales en las estadísticas de recuento de palabras en C++."
type: docs
weight: 33000
url: /es/cpp/aspose.words/document/get_includetextboxesfootnotesendnotesinstat/
---
## Document::get_IncludeTextboxesFootnotesEndnotesInStat method


Especifica si se deben incluir cuadros de texto, notas al pie y notas finales en las estadísticas de recuento de palabras.

```cpp
bool Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat()
```


## Ejemplos



Muestra cómo incluir o excluir cuadros de texto, notas al pie y notas finales de las estadísticas de recuento de palabras.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Lorem ipsum");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"sit amet");

// Por defecto, la opción está establecida en 'false'.
doc->UpdateWordCount();
// Recuento de palabras sin cuadros de texto, notas al pie y notas finales.
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Words());

doc->set_IncludeTextboxesFootnotesEndnotesInStat(true);
doc->UpdateWordCount();
// Recuento de palabras con cuadros de texto, notas al pie y notas finales.
ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Words());
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
