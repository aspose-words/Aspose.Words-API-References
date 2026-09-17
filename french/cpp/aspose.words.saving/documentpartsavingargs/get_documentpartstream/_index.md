---
title: "méthode Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream"
linktitle: "get_DocumentPartStream"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "méthode Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream. Permet de spécifier le flux où la partie du document sera enregistrée en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartstream/
---
## DocumentPartSavingArgs::get_DocumentPartStream method


Permet de spécifier le flux où la partie du document sera enregistrée.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream() const
```

## Remarques


Cette propriété vous permet d’enregistrer les parties du document dans des flux au lieu de fichiers lors de l’exportation HTML.

La valeur par défaut est **null**. Lorsque cette propriété est **null**, la partie du document sera enregistrée dans un fichier spécifié dans la propriété [DocumentPartFileName](../get_documentpartfilename/).

Lorsque l’enregistrement vers un flux au format HTML est demandé par [Save()](../) ou [Save()](../) et que la première partie du document est sur le point d’être enregistrée, Aspose.Words suggère ici le flux de sortie principal initialement fourni par l’appelant.

Lors de l’enregistrement au format EPUB, qui est un format conteneur basé sur HTML, [DocumentPartStream](./) ne peut pas être spécifié car toutes les parties subsidiaires seront encapsulées dans un seul paquet de sortie.

## Voir aussi

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
