---
title: "Aspose::Words::Fields::FieldEQ::AsOfficeMath méthode"
linktitle: "AsOfficeMath"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldEQ::AsOfficeMath. Retourne l'objet Office Math correspondant au champ EQ en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ::AsOfficeMath method


Retourne l'objet Office [Math](../../../aspose.words.math/) correspondant au champ EQ.

```cpp
System::SharedPtr<Aspose::Words::Math::OfficeMath> Aspose::Words::Fields::FieldEQ::AsOfficeMath()
```


### ReturnValue

Retourne **null** si le code du champ est vide ou invalide, sinon une instance [OfficeMath](../../../aspose.words.math/officemath/).

## Exemples



Montre comment remplacer le champ EQ par Office [Math](../../../aspose.words.math/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - EQ.docx");
System::SharedPtr<Aspose::Words::Fields::FieldEQ> fieldEQ = doc->get_Range()->get_Fields()->LINQ_OfType<System::SharedPtr<Aspose::Words::Fields::FieldEQ> >()->LINQ_First();

System::SharedPtr<Aspose::Words::Math::OfficeMath> officeMath = fieldEQ->AsOfficeMath();

fieldEQ->get_Start()->get_ParentNode()->InsertBefore<System::SharedPtr<Aspose::Words::Math::OfficeMath>>(officeMath, fieldEQ->get_Start());
fieldEQ->Remove();

doc->Save(get_ArtifactsDir() + u"Field.EQAsOfficeMath.docx");
```

## Voir aussi

* Class [OfficeMath](../../../aspose.words.math/officemath/)
* Class [FieldEQ](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
