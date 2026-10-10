---
title: "Aspose::Words::JoinRunsOptions classe"
linktitle: "JoinRunsOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::JoinRunsOptions classe. Fournit des indicateurs de configuration pour l'opération de fusion des runs en C++."
type: docs
weight: 38500
url: /fr/cpp/aspose.words/joinrunsoptions/
---
## JoinRunsOptions class


Fournit des indicateurs de configuration pour l'opération de jointure des runs.

```cpp
class JoinRunsOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_IgnoreInsignificant](./get_ignoreinsignificant/)() const | Vrai indique que les attributs insignifiants de tous les runs seront ignorés lors de la fusion des runs avec le même formatage. |
| [get_IgnoreRedundant](./get_ignoreredundant/)() const | Vrai indique que les attributs redondants de tous les runs seront ignorés lors de la fusion des runs avec le même formatage. |
| [get_IgnoreSpacing](./get_ignorespacing/)() const | Vrai indique que les attributs d'espacement de tous les runs seront ignorés lors de la fusion des runs avec le même formatage. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [JoinRunsOptions](./joinrunsoptions/)() |  |
| [set_IgnoreInsignificant](./set_ignoreinsignificant/)(bool) | Vrai indique que les attributs insignifiants de tous les runs seront ignorés lors de la fusion des runs avec le même formatage. |
| [set_IgnoreRedundant](./set_ignoreredundant/)(bool) | Vrai indique que les attributs redondants de tous les runs seront ignorés lors de la fusion des runs avec le même formatage. |
| [set_IgnoreSpacing](./set_ignorespacing/)(bool) | Vrai indique que les attributs d'espacement de tous les runs seront ignorés lors de la fusion des runs avec le même formatage. |
| static [Type](./type/)() |  |

## Exemples



Montre comment fusionner des runs avec le même formatage tout en ignorant les attributs redondants et insignifiants.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez des runs avec un formatage visible identique mais quelques différences internes.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// Vérifiez les runs avant la fusion.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// Configurez les options pour ignorer les attributs redondants et insignifiants lors de la fusion.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// Ignorez les propriétés de run redondantes qui n'affectent pas l'apparence.
options->set_IgnoreInsignificant(true);
// Ignorez les différences insignifiantes comme les runs composés uniquement d'espaces.

// Fusionnez les segments qui ont le même formatage visible en utilisant les options étendues.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// Vérifiez que les segments ont été fusionnés avec succès.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
