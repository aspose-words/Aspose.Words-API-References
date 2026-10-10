---
title: "Aspose::Words::Comparing::AdvancedCompareOptions class"
linktitle: "AdvancedCompareOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions class. Permite establecer opciones avanzadas de comparación en C++."
type: docs
weight: 500
url: /es/cpp/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class


Permite establecer opciones avanzadas de comparación.

```cpp
class AdvancedCompareOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [AdvancedCompareOptions](./advancedcompareoptions/)() |  |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() const | Especifica si se debe ignorar la diferencia en el Id único de DrawingML. |
| [get_IgnoreStoreItemId](./get_ignorestoreitemid/)() const | Especifica si se debe ignorar la diferencia en el Id del elemento almacenado de StructuredDocumentTag. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Método set para [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreStoreItemId](./set_ignorestoreitemid/)(bool) | Método set para [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId](./get_ignorestoreitemid/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo comparar SDT con el mismo contenido pero con un id de elemento almacenado diferente.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Configure opciones para comparar SDT con el mismo contenido pero con un id de elemento almacenado diferente.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## Ver también

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
