---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels method"
linktitle: "get_SimplifyListLabels"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels method. Spécifie si le programme doit simplifier les libellés de listes lorsqu'un formatage de libellé complexe n'est pas correctement représenté en texte brut. Si la valeur est true, les libellés de listes numérotées sont écrits au format numérique simple et les libellés de listes à puces en caractères ASCII simples. La valeur par défaut est false en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.saving/txtsaveoptions/get_simplifylistlabels/
---
## TxtSaveOptions::get_SimplifyListLabels method


Spécifie si le programme doit simplifier les libellés de listes dans le cas où un formatage de libellé complexe n'est pas correctement représenté en texte brut. Si la valeur est **true**, les libellés des listes numérotées sont écrits en format numérique simple et les libellés des listes à puces en caractères ASCII simples. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels() const
```


## Exemples



Montre comment modifier l'apparence des listes lors de l'enregistrement d'un document en texte brut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez une liste à puces avec cinq niveaux d'indentation.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 3");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 4");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 5");

// Créez un objet "TxtSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Définissez la propriété "SimplifyListLabels" sur "true" pour convertir certaines listes
// les symboles en caractères ASCII plus simples, tels que '*', 'o', '+', '>', etc.
// Définissez la propriété "SimplifyListLabels" sur "false" pour conserver le plus possible de symboles de listes originaux.
txtSaveOptions->set_SimplifyListLabels(simplifyListLabels);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt");

System::String newLine = System::Environment::get_NewLine();
if (simplifyListLabels)
{
    ASSERT_EQ(System::String::Format(u"* Item 1{0}", newLine) + System::String::Format(u"  > Item 2{0}", newLine) + System::String::Format(u"    + Item 3{0}", newLine) + System::String::Format(u"      - Item 4{0}", newLine) + System::String::Format(u"        o Item 5{0}", newLine), docText);
}
else
{
    ASSERT_EQ(System::String::Format(u"· Item 1{0}", newLine) + System::String::Format(u"o Item 2{0}", newLine) + System::String::Format(u"§ Item 3{0}", newLine) + System::String::Format(u"· Item 4{0}", newLine) + System::String::Format(u"o Item 5{0}", newLine), docText);
}
```

## Voir aussi

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
