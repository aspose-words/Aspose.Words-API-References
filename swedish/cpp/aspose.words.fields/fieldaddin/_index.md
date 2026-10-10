---
title: "Aspose::Words::Fields::FieldAddIn klass"
linktitle: "FieldAddIn"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldAddIn klass. Implementerar ADDIN-fältet i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.fields/fieldaddin/
---
## FieldAddIn class


Implementerar ADDIN-fältet.

```cpp
class FieldAddIn : public Aspose::Words::Fields::Field
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |

## Exempel



Visar hur man bearbetar ett ADDIN-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - ADDIN.docx");

// Aspose.Words stöder inte att infoga ADDIN-fält, men vi kan fortfarande läsa in och läsa dem.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAddIn>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u" ADDIN \"My value\" ", field->GetFieldCode());
```

## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
