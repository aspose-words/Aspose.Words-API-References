---
title: "Metodo Aspose::Words::Fields::FieldImport::get_IsLinked"
linktitle: "get_IsLinked"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldImport::get_IsLinked. Restituisce o imposta se ridurre le dimensioni del file evitando di memorizzare i dati grafici nel documento in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fields/fieldimport/get_islinked/
---
## FieldImport::get_IsLinked method


Ottiene o imposta se ridurre le dimensioni del file non memorizzando i dati grafici nel documento.

```cpp
bool Aspose::Words::Fields::FieldImport::get_IsLinked() override
```


## Esempi



Mostra come inserire immagini usando i campi IMPORT e INCLUDEPICTURE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono due tipi di campo simili che possiamo usare per visualizzare immagini collegate dal file system locale.
// 1 -  Il campo INCLUDEPICTURE:
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// Applica il filtro PNG32.FLT.
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  Il campo IMPORT:
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## Vedi anche

* Class [FieldImport](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
