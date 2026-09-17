---
title: "Aspose::Words::NumSpacing enum"
linktitle: "NumSpacing"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::NumSpacing enum. Spécifie les valeurs possibles dans lesquelles l’espacement des chiffres peut être affiché en C++."
type: docs
weight: 103500
url: /fr/cpp/aspose.words/numspacing/
---
## NumSpacing enum


Spécifie les valeurs possibles dans lesquelles l'espacement des chiffres peut être affiché.

```cpp
enum class NumSpacing
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Default | 0 | Spécifie que les chiffres sont affichés dans la forme par défaut de la police. |
| Proportionnel | 1 | Spécifie que les formes des chiffres conçues comme proportionnellement espacées sont affichées si la police les prend en charge. |
| Tabulaire | 2 | Spécifie que les formes des chiffres conçues comme tabulaires sont affichées si la police le prend en charge. |


## Exemples



Montre comment définir le type d'espacement du chiffre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cet effet n'est pris en charge que dans les versions récentes de MS Word.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
