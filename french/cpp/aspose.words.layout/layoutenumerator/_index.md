---
title: "classe Aspose::Words::Layout::LayoutEnumerator"
linktitle: "LayoutEnumerator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Layout::LayoutEnumerator. Énumère les entités de mise en page d'un document. Vous pouvez utiliser cette classe pour parcourir le modèle de mise en page. Les propriétés disponibles sont le type, la géométrie, le texte et l'index de page où l'entité est rendue, ainsi que la structure globale et les relations. Utilisez la combinaison de GetEntity() et Current pour vous déplacer vers l'entité qui correspond à un nœud de document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class


Énumère les entités de mise en page d'un document. Vous pouvez utiliser cette classe pour parcourir le modèle de mise en page. Les propriétés disponibles sont le type, la géométrie, le texte et l'index de page où l'entité est rendue, ainsi que la structure globale et les relations. Utilisez la combinaison de [GetEntity()](../) et [Current](./get_current/) pour vous déplacer vers l'entité qui correspond à un nœud de document. Pour en savoir plus, consultez l'article de documentation [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutEnumerator : public System::Object,
                         public System::Details::EnumeratorBasedIterator<System::SharedPtr<System::Object>>,
                         private System::Details::IteratorPointerUpdater<System::SharedPtr<System::Object>, false>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [CloneIterator](./cloneiterator/)() const override |  |
| [get_Current](./get_current/)() const | Obtient ou définit la position actuelle dans le modèle de mise en page. Cette propriété renvoie un objet opaque qui correspond à l'entité de mise en page actuelle. |
| [get_Document](./get_document/)() const | Obtient le document que cette instance énumère. |
| [get_Kind](./get_kind/)() | Obtient le type de l'entité actuelle. Cela peut être une chaîne vide mais jamais **null**. |
| [get_PageIndex](./get_pageindex/)() | Obtient l'index basé sur 1 d'une page qui contient l'entité actuelle. |
| [get_Rectangle](./get_rectangle/)() | Renvoie le rectangle englobant de l'entité actuelle relatif au coin supérieur gauche de la page (en points). |
| [get_Text](./get_text/)() | Obtient le texte de l'entité span actuelle. Lève une exception pour les autres types d'entité. |
| [get_Type](./get_type/)() | Obtient le type de l'entité actuelle. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtient une propriété nommée de l'entité. |
| [IncrementIterator](./incrementiterator/)() override |  |
| [InitializeIterator](./initializeiterator/)() override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutEnumerator](./layoutenumerator/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Initialise une nouvelle instance de cette classe. |
| [MoveFirstChild](./movefirstchild/)() | Se déplace vers la première entité enfant. |
| [MoveLastChild](./movelastchild/)() | Se déplace vers la dernière entité enfant. |
| [MoveNext](./movenext/)() | Se déplace vers l'entité sœur suivante dans l'ordre visuel. Lors de l'itération des lignes d'un paragraphe réparti sur plusieurs pages, cette méthode ne passe pas à la page suivante mais se déplace vers l'entité suivante sur la même page. |
| [MoveNextLogical](./movenextlogical/)() | Se déplace vers l'entité sœur suivante dans un ordre logique. Lors de l'itération des lignes d'un paragraphe réparti sur plusieurs pages, cette méthode se déplacera vers la ligne suivante même si elle se trouve sur une autre page. |
| [MoveParent](./moveparent/)() | Se déplace vers l'entité parent. |
| [MoveParent](./moveparent/)(Aspose::Words::Layout::LayoutEntityType) | Se déplace vers l'entité parent du type spécifié. |
| [MovePrevious](./moveprevious/)() | Se déplace vers l'entité sœur précédente. |
| [MovePreviousLogical](./movepreviouslogical/)() | Se déplace vers l'entité sœur précédente dans un ordre logique. Lors de l'itération des lignes d'un paragraphe réparti sur plusieurs pages, cette méthode se déplacera vers la ligne précédente même si elle se trouve sur une autre page. |
| [Reset](./reset/)() | Déplace l'énumérateur vers la première page du document. |
| [set_Current](./set_current/)(const System::SharedPtr\<System::Object\>\&) | Mutateur pour [Aspose::Words::Layout::LayoutEnumerator::get_Current](./get_current/). |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
