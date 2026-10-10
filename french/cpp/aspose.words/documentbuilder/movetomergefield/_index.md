---
title: "Aspose::Words::DocumentBuilder::MoveToMergeField méthode"
linktitle: "MoveToMergeField"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::MoveToMergeField méthode. Déplace le curseur à une position juste après le champ de fusion spécifié et supprime le champ de fusion en C++."
type: docs
weight: 58000
url: /fr/cpp/aspose.words/documentbuilder/movetomergefield/
---
## DocumentBuilder::MoveToMergeField(const System::String\&) method


Déplace le curseur vers une position juste après le champ de fusion spécifié et supprime le champ de fusion.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldName | const System::String\& | Le nom du champ de fusion de courrier, insensible à la casse. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.
## Remarques


Notez que cette méthode supprime le champ de fusion du document après avoir déplacé le curseur.

## Exemples



Montre comment remplir les MERGEFIELDs avec des données à l'aide d'un constructeur de document au lieu d'une fusion de courrier.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez quelques MERGEFIELDS, qui acceptent des données provenant de colonnes du même nom dans une source de données lors d'une fusion de courrier,
// et remplissez-les ensuite manuellement.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## Voir aussi

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToMergeField(const System::String\&, bool, bool) method


Déplace le champ de fusion vers le champ de fusion spécifié.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName, bool isAfter, bool isDeleteField)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldName | const System::String\& | Le nom du champ de fusion de courrier, insensible à la casse. |
| isAfter | bool | Lorsque **true**, déplace le curseur pour qu'il soit après la fin du champ. Lorsque **false**, déplace le curseur pour qu'il soit avant le début du champ. |
| isDeleteField | bool | Lorsque **true**, supprime le champ de fusion. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.

## Exemples



Montre comment insérer des champs et déplacer le curseur du constructeur de document vers eux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// Déplacez le curseur vers le premier MERGEFIELD.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// Notez que le curseur est placé immédiatement après le premier MERGEFIELD, et avant le deuxième.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// Si nous souhaitons modifier le code de champ ou le contenu du champ à l'aide du constructeur,
// son curseur devrait être à l'intérieur d'un champ.
// Pour le placer à l'intérieur d'un champ, nous devrions appeler la méthode MoveTo du constructeur de document
// et passer le nœud de début ou de séparateur du champ comme argument.
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```

## Voir aussi

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
