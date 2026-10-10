---
title: "Constructeur Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator"
linktitle: "LayoutEnumerator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Constructeur Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator. Initialise une nouvelle instance de cette classe en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.layout/layoutenumerator/layoutenumerator/
---
## LayoutEnumerator::LayoutEnumerator constructor


Initialise une nouvelle instance de cette classe.

```cpp
Aspose::Words::Layout::LayoutEnumerator::LayoutEnumerator(const System::SharedPtr<Aspose::Words::Document> &document)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| document | const System::SharedPtr\<Aspose::Words::Document\>\& | Un document dont le modèle de mise en page doit être énuméré. |
## Remarques


Si le modèle de mise en page du document n'a pas été construit, l'énumérateur appelle [UpdatePageLayout](../../../aspose.words/document/updatepagelayout/) pour le créer.

Chaque fois que le document est mis à jour et qu'un nouveau modèle de mise en page est créé, un nouvel énumérateur doit être utilisé pour y accéder.

## Voir aussi

* Class [Document](../../../aspose.words/document/)
* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
