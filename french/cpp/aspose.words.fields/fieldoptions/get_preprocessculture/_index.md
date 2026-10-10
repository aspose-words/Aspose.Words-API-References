---
title: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture méthode"
linktitle: "get_PreProcessCulture"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture méthode. Obtient ou définit la culture pour prétraiter les valeurs des champs en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words.fields/fieldoptions/get_preprocessculture/
---
## FieldOptions::get_PreProcessCulture method


Obtient ou définit la culture à utiliser pour prétraiter les valeurs de champ.

```cpp
const System::SharedPtr<System::Globalization::CultureInfo> & Aspose::Words::Fields::FieldOptions::get_PreProcessCulture() const
```

## Remarques


Actuellement, cette propriété n'affecte que la valeur du champ [FieldDocProperty](../../fielddocproperty/).

La valeur par défaut est **null**. Lorsque cette propriété est définie sur **null**, la valeur du champ [FieldDocProperty](../../fielddocproperty/) est prétraitée avec la culture contrôlée par la propriété [FieldUpdateCultureSource](../get_fieldupdateculturesource/).

## Exemples



Montre comment définir la culture de prétraitement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez la culture selon laquelle certains champs formateront leurs valeurs affichées.
doc->get_FieldOptions()->set_PreProcessCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" DOCPROPERTY CreateTime");

// Le champ DOCPROPERTY affichera son résultat formaté selon la culture de prétraitement
// nous l'avons définie sur l'allemand. Le champ affichera la date/heure en utilisant le format "dd.mm.yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}")->get_Success());

doc->get_FieldOptions()->set_PreProcessCulture(System::Globalization::CultureInfo::get_InvariantCulture());
field->Update();

// Après être passé à la culture invariante, le champ DOCPROPERTY utilisera le format "mm/dd/yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}")->get_Success());
```

## Voir aussi

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
