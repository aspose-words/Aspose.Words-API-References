---
title: "Aspose::Words::Document::get_VersionsCount méthode"
linktitle: "get_VersionsCount"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::get_VersionsCount. Obtient le nombre de versions du document qui ont été stockées dans le document DOC en C++."
type: docs
weight: 57000
url: /fr/cpp/aspose.words/document/get_versionscount/
---
## Document::get_VersionsCount method


Obtient le nombre de versions du document qui ont été stockées dans le document DOC.

```cpp
int32_t Aspose::Words::Document::get_VersionsCount()
```

## Remarques


Les versions dans Microsoft Word sont accessibles via le menu Fichier/Versions. Microsoft Word ne prend en charge les versions que pour les fichiers DOC.

Cette propriété permet de détecter s'il y avait des versions du document stockées dans ce document avant son ouverture dans Aspose.Words. Aspose.Words ne fournit aucun autre support pour les versions de documents. Si vous enregistrez ce document avec Aspose.Words, le document sera enregistré sans versions.

## Exemples



Montre comment travailler avec la fonctionnalité de comptage des versions des anciens documents Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Versions.doc");

// Nous pouvons lire cette propriété d'un document, mais nous ne pouvons pas la conserver lors de l'enregistrement.
ASSERT_EQ(4, doc->get_VersionsCount());

doc->Save(get_ArtifactsDir() + u"Document.VersionsCount.doc");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.VersionsCount.doc");

ASSERT_EQ(0, doc->get_VersionsCount());
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
