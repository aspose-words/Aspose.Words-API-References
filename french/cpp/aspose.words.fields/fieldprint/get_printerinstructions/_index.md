---
title: "Aspose::Words::Fields::FieldPrint::get_PrinterInstructions méthode"
linktitle: "get_PrinterInstructions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldPrint::get_PrinterInstructions méthode. Obtient ou définit les caractères de code de contrôle spécifiques à l'imprimante ou les instructions PostScript en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldprint/get_printerinstructions/
---
## FieldPrint::get_PrinterInstructions method


Obtient ou définit les caractères de code de contrôle spécifiques à l'imprimante ou les instructions PostScript.

```cpp
System::String Aspose::Words::Fields::FieldPrint::get_PrinterInstructions()
```


## Exemples



Montre comment insérer un champ PRINT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"My paragraph");

// Le champ PRINT peut envoyer des instructions à l'imprimante.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrint>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPrint, true));

// Définissez la zone sur laquelle l'imprimante doit exécuter les instructions.
// Dans ce cas, ce sera le paragraphe qui contient notre champ PRINT.
field->set_PostScriptGroup(u"para");

// Lorsque nous utilisons une imprimante qui prend en charge PostScript pour imprimer notre document,
// cette commande rendra toute la zone que nous avons spécifiée dans "field.PostScriptGroup" blanche.
field->set_PrinterInstructions(u"erasepage");

ASSERT_EQ(u" PRINT  erasepage \\p para", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.PRINT.docx");
```

## Voir aussi

* Class [FieldPrint](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
