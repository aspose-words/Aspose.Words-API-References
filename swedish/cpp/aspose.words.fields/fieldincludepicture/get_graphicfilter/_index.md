---
title: "Aspose::Words::Fields::FieldIncludePicture::get_GraphicFilter metod"
linktitle: "get_GraphicFilter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIncludePicture::get_GraphicFilter metod. Hämtar eller anger namnet på filtret för formatet på den grafik som ska infogas i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldincludepicture/get_graphicfilter/
---
## FieldIncludePicture::get_GraphicFilter method


Hämtar eller anger namnet på filtret för formatet på grafiken som ska infogas.

```cpp
System::String Aspose::Words::Fields::FieldIncludePicture::get_GraphicFilter()
```


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

* Class [FieldIncludePicture](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
