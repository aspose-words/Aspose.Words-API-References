---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName méthode"
linktitle: "get_DocumentPartFileName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName méthode. Obtient ou définit le nom de fichier (sans le chemin) où la partie du document sera enregistrée en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartfilename/
---
## DocumentPartSavingArgs::get_DocumentPartFileName method


Obtient ou définit le nom de fichier (sans le chemin) où la partie du document sera enregistrée.

```cpp
System::String Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName() const
```

## Remarques


Cette propriété vous permet de redéfinir la façon dont les noms de fichiers des parties de document sont générés lors de l'exportation vers HTML ou EPUB.

Lorsque le rappel est invoqué, cette propriété contient le nom de fichier généré par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour enregistrer la partie du document dans un fichier différent. Notez que le nom de fichier pour chaque partie doit être unique.

[DocumentPartFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

## Voir aussi

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
