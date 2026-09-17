---
title: "Méthode Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles"
linktitle: "get_AlwaysCompressMetafiles"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles. Lorsqu'elle est false, les petits métafichiers ne sont pas compressés pour des raisons de performance. La valeur par défaut est true, tous les métafichiers sont compressés quelle que soit leur taille en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/docsaveoptions/get_alwayscompressmetafiles/
---
## DocSaveOptions::get_AlwaysCompressMetafiles method


Lorsque **false**, les petits métafichiers ne sont pas compressés pour des raisons de performances. La valeur par défaut est **true**, tous les métafichiers sont compressés quel que soit leur taille.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles() const
```


## Exemples



Montre comment modifier la compression des métafichiers dans un document lors de l'enregistrement.
```cpp
// Ouvrez un document contenant une formule Microsoft Equation 3.0.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Microsoft equation object.docx");

// Lorsque nous enregistrons un document, les petits métafichiers ne sont pas compressés pour des raisons de performance.
// Nous pouvons définir un indicateur dans un objet SaveOptions pour compresser chaque métafichier lors de l'enregistrement.
// Certains éditeurs comme LibreOffice ne peuvent pas lire les métafichiers non compressés.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_AlwaysCompressMetafiles(compressAllMetafiles);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

## Voir aussi

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
