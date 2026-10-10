---
title: "Aspose::Words::Document::RemoveCustomizations method"
linktitle: "RemoveCustomizations"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::RemoveCustomizations method. Supprime les personnalisations de la barre d'outils et des commandes clavier du document en C++."
type: docs
weight: 67750
url: /fr/cpp/aspose.words/document/removecustomizations/
---
## Document::RemoveCustomizations method


Supprime les personnalisations de la barre d'outils et des raccourcis clavier du document.

```cpp
void Aspose::Words::Document::RemoveCustomizations()
```


## Exemples



Montre comment supprimer les personnalisations de la barre d'outils et des commandes clavier du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Customized menu.docx");

// Supprime toutes les personnalisations UI du document, y compris les entrées personnalisées du menu contextuel.
doc->RemoveCustomizations();

doc->Save(get_ArtifactsDir() + u"Document.RemoveCustomizations.docx");
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
