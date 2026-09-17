---
title: "Classe Aspose::Words::MailMerging::MappedDataFieldCollection"
linktitle: "MappedDataFieldCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::MailMerging::MappedDataFieldCollection. Permet de mapper automatiquement entre les noms de champs de votre source de données et les noms des champs de publipostage dans le document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class


Permet de mapper automatiquement les noms des champs de votre source de données aux noms des champs de fusion de courrier dans le document. Pour en savoir plus, consultez l'article de documentation [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MappedDataFieldCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Ajoute un nouveau mappage de champ. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Supprime tous les éléments de la collection. |
| [ContainsKey](./containskey/)(const System::String\&) | Détermine si un mappage du champ spécifié dans le document existe dans la collection. |
| [ContainsValue](./containsvalue/)(const System::String\&) | Détermine si un mappage du champ spécifié dans la source de données existe dans la collection. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtient le nombre d’éléments contenus dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur de dictionnaire qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtient ou définit le nom du champ dans la source de données associé au champ de publipostage spécifié. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Obtient ou définit le nom du champ dans la source de données associé au champ de publipostage spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Supprime un mappage de champ. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Remarques


Ceci est implémenté comme une collection de clés de chaîne vers des valeurs de chaîne. Les clés sont les noms des champs de publipostage dans le document et les valeurs sont les noms des champs de votre source de données.

## Voir aussi

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
