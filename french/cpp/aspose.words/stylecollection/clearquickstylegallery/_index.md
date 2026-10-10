---
title: "Aspose::Words::StyleCollection::ClearQuickStyleGallery méthode"
linktitle: "ClearQuickStyleGallery"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::StyleCollection::ClearQuickStyleGallery méthode. Supprime tous les styles du panneau Quick Style Gallery en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection::ClearQuickStyleGallery method


Supprime tous les styles du panneau Quick [Style](../../style/) Gallery.

```cpp
void Aspose::Words::StyleCollection::ClearQuickStyleGallery()
```


## Exemples



Montre comment supprimer des styles du panneau [Style](../../style/) Gallery.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
// Notez que la suppression des styles ne fonctionne pour le moment qu'avec le format DOCX.
doc->get_Styles()->ClearQuickStyleGallery();

doc->Save(get_ArtifactsDir() + u"Styles.RemoveStylesFromStyleGallery.docx");
```

## Voir aussi

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
