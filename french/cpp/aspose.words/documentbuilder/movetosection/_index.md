---
title: "Méthode Aspose::Words::DocumentBuilder::MoveToSection"
linktitle: "MoveToSection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::MoveToSection. Déplace le curseur au début du corps dans une section spécifiée en C++."
type: docs
weight: 60000
url: /fr/cpp/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder::MoveToSection method


Déplace le curseur vers le début du corps dans une section spécifiée.

```cpp
void Aspose::Words::DocumentBuilder::MoveToSection(int32_t sectionIndex)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| sectionIndex | int32_t | L'index de la section vers laquelle se déplacer. |
## Remarques


Lorsque *sectionIndex* est supérieur ou égal à 0, il indique un index depuis le début du document, 0 étant la première section. Lorsque *sectionIndex* est inférieur à 0, il indique un index depuis la fin du document, -1 étant la dernière section.

Le curseur est déplacé vers le premier paragraphe du [Body](../../body/) de la section spécifiée.

## Voir aussi

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
