---
title: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat méthode"
linktitle: "get_LegacyNumberFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat method. Obtient ou définit la valeur indiquant si le format de nombre hérité (antérieur à AW 13.10) pour les champs est activé ou non en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.fields/fieldoptions/get_legacynumberformat/
---
## FieldOptions::get_LegacyNumberFormat method


Obtient ou définit la valeur indiquant si le format numérique hérité (antérieur à AW 13.10) pour les champs est activé ou non.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat() const
```

## Remarques


Lorsque cette propriété est définie sur **true**, le symbole de modèle \"#\" fonctionne comme dans .net : remplace le signe dièse par le chiffre correspondant s'il est présent ; sinon, aucun symbole n'apparaît dans la chaîne résultante.

Lorsque cette propriété est définie sur **false**, le symbole de modèle \"#\" fonctionne comme MS Word : cet élément de format spécifie les positions numériques requises à afficher dans le résultat. Si le résultat ne comprend pas de chiffre à cette position, MS Word affiche un espace. Par exemple, { = 9 + 6 \\# $### } affiche $ 15.

La valeur par défaut est **false**.

## Exemples



Montre comment activer le formatage de nombre hérité pour les champs.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3 \\# $##");

ASSERT_EQ(u"$ 5", field->get_Result());

doc->get_FieldOptions()->set_LegacyNumberFormat(true);
field->Update();

ASSERT_EQ(u"$5", field->get_Result());
```

## Voir aussi

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
