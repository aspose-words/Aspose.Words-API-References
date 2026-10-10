---
title: "Aspose::Words::Fields::FieldIncludePicture::get_GraphicFilter méthode"
linktitle: "get_GraphicFilter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldIncludePicture::get_GraphicFilter méthode. Obtient ou définit le nom du filtre pour le format du graphique à insérer en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldincludepicture/get_graphicfilter/
---
## FieldIncludePicture::get_GraphicFilter method


Obtient ou définit le nom du filtre pour le format du graphique à insérer.

```cpp
System::String Aspose::Words::Fields::FieldIncludePicture::get_GraphicFilter()
```


## Exemples



Montre comment insérer des images à l'aide des champs IMPORT et INCLUDEPICTURE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ci-dessous, deux types de champs similaires que nous pouvons utiliser pour afficher des images liées depuis le système de fichiers local.
// 1 -  Le champ INCLUDEPICTURE :
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// Appliquer le filtre PNG32.FLT.
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  Le champ IMPORT :
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## Voir aussi

* Class [FieldIncludePicture](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
