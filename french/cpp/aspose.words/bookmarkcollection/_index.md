---
title: "Aspose::Words::BookmarkCollection classe"
linktitle: "BookmarkCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BookmarkCollection classe. Une collection d'objets Bookmark qui représentent les signets dans la plage spécifiée. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/bookmarkcollection/
---
## BookmarkCollection class


Une collection d'objets [Bookmark](../bookmark/) qui représentent les signets dans la plage spécifiée. Pour en savoir plus, consultez l'article de documentation [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarkCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bookmark>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clear](./clear/)() | Supprime tous les signets de cette collection et du document. |
| [get_Count](./get_count/)() | Renvoie le nombre de signets dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Renvoie un signet à l'index spécifié. |
| [idx_get](./idx_get/)(const System::String\&) | Renvoie un signet par son nom. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) | Supprime le signet spécifié du document. |
| [Remove](./remove/)(const System::String\&) | Supprime un signet avec le nom spécifié. |
| [RemoveAt](./removeat/)(int32_t) | Supprime un signet à l'index spécifié. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
