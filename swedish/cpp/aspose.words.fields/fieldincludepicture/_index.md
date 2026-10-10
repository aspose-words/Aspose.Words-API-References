---
title: "Aspose::Words::Fields::FieldIncludePicture klass"
linktitle: "FieldIncludePicture"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIncludePicture klass. Implementerar INCLUDEPICTURE-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 57000
url: /sv/cpp/aspose.words.fields/fieldincludepicture/
---
## FieldIncludePicture class


Implementerar INCLUDEPICTURE-fältet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIncludePicture : public Aspose::Words::Fields::Field,
                            public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                            public Aspose::Words::Fields::IFieldIncludePictureCode
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_GraphicFilter](./get_graphicfilter/)() | Hämtar eller anger namnet på filtret för formatet på grafiken som ska infogas. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLinked](./get_islinked/)() override | Hämtar eller anger om filstorleken ska minskas genom att inte lagra grafikdata med dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_ResizeHorizontally](./get_resizehorizontally/)() | Hämtar eller anger om bilden ska skalas horisontellt från källan. |
| [get_ResizeVertically](./get_resizevertically/)() | Hämtar eller anger om bilden ska skalas vertikalt från källan. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_SourceFullName](./get_sourcefullname/)() override | Hämtar eller anger bildens plats med en IRI. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_GraphicFilter](./set_graphicfilter/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIncludePicture::get_GraphicFilter](./get_graphicfilter/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLinked](./set_islinked/)(bool) | Sättare för [Aspose::Words::Fields::FieldIncludePicture::get_IsLinked](./get_islinked/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ResizeHorizontally](./set_resizehorizontally/)(bool) | Sättare för [Aspose::Words::Fields::FieldIncludePicture::get_ResizeHorizontally](./get_resizehorizontally/). |
| [set_ResizeVertically](./set_resizevertically/)(bool) | Sättare för [Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically](./get_resizevertically/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Inställare för [Aspose::Words::Fields::FieldIncludePicture::get_SourceFullName](./get_sourcefullname/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |

## Exempel



Visar hur man infogar bilder med IMPORT- och INCLUDEPICTURE-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan finns två liknande fälttyper som vi kan använda för att visa bilder länkade från det lokala filsystemet.
// 1 -  INCLUDEPICTURE-fältet:
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// Applicera PNG32.FLT-filtret.
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  IMPORT-fältet:
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
