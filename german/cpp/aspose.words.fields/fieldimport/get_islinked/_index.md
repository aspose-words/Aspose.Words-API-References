---
title: "Aspose::Words::Fields::FieldImport::get_IsLinked Methode"
linktitle: "get_IsLinked"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldImport::get_IsLinked Methode. Ruft ab oder legt fest, ob die Dateigröße reduziert werden soll, indem Grafikdaten nicht mit dem Dokument in C++ gespeichert werden."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldimport/get_islinked/
---
## FieldImport::get_IsLinked method


Ermittelt oder legt fest, ob die Dateigröße reduziert werden soll, indem Grafikdaten nicht im Dokument gespeichert werden.

```cpp
bool Aspose::Words::Fields::FieldImport::get_IsLinked() override
```


## Beispiele



Zeigt, wie Bilder mit den Feldern IMPORT und INCLUDEPICTURE eingefügt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei ähnliche Feldtypen, die wir verwenden können, um Bilder anzuzeigen, die aus dem lokalen Dateisystem verlinkt sind.
// 1 -  Das INCLUDEPICTURE-Feld:
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// Wenden Sie den PNG32.FLT-Filter an.
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  Das IMPORT-Feld:
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## Siehe auch

* Class [FieldImport](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
