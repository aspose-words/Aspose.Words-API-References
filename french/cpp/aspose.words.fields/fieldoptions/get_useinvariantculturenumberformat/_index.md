---
title: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat méthode"
linktitle: "get_UseInvariantCultureNumberFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat méthode. Obtient ou définit la valeur indiquant que le format numérique est analysé en utilisant la culture invariante ou non en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words.fields/fieldoptions/get_useinvariantculturenumberformat/
---
## FieldOptions::get_UseInvariantCultureNumberFormat method


Obtient ou définit la valeur indiquant si le format numérique est analysé en utilisant la culture invariante ou non.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat() const
```

## Remarques


Lorsque cette propriété est définie sur **true**, le format numérique est pris à partir d'une culture invariante.

Lorsque cette propriété est définie sur **false**, le format numérique est pris à partir de la culture du thread actuel.

La valeur par défaut est **false**.

## Exemples



Montre comment formater les nombres selon la culture invariante.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::Threading::Thread::get_CurrentThread()->set_CurrentCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" = 1234567,89 \\# $#,###,###.##");
field->Update();

// Parfois, les champs peuvent ne pas formater correctement leurs nombres sous certaines cultures.
ASSERT_FALSE(doc->get_FieldOptions()->get_UseInvariantCultureNumberFormat());
ASSERT_EQ(u"$1.234.567,89 ,     ", field->get_Result());

// Pour résoudre cela, nous pourrions changer la culture pour l'ensemble du thread.
// Une autre façon de résoudre cela est de définir ce drapeau,
// qui fait que tous les champs utilisent la culture invariante lors du formatage des nombres.
// Cette méthode nous permet d'éviter de changer la culture pour l'ensemble du thread.
doc->get_FieldOptions()->set_UseInvariantCultureNumberFormat(true);
field->Update();
ASSERT_EQ(u"$1.234.567,89", field->get_Result());
```

## Voir aussi

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
