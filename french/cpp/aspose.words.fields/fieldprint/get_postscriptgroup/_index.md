---
title: "Méthode Aspose::Words::Fields::FieldPrint::get_PostScriptGroup"
linktitle: "get_PostScriptGroup"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldPrint::get_PostScriptGroup. Obtient ou définit le rectangle de dessin sur lequel les instructions PostScript opèrent en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldprint/get_postscriptgroup/
---
## FieldPrint::get_PostScriptGroup method


Obtient ou définit le rectangle de dessin sur lequel les instructions PostScript opèrent.

```cpp
System::String Aspose::Words::Fields::FieldPrint::get_PostScriptGroup()
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
