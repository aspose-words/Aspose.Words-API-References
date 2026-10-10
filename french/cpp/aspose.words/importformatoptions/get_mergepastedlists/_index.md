---
title: "Aspose::Words::ImportFormatOptions::get_MergePastedLists méthode"
linktitle: "get_MergePastedLists"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ImportFormatOptions::get_MergePastedLists méthode. Obtient ou définit une valeur booléenne qui indique si les listes collées seront fusionnées avec les listes environnantes. La valeur par défaut est false en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/importformatoptions/get_mergepastedlists/
---
## ImportFormatOptions::get_MergePastedLists method


Obtient ou définit une valeur booléenne qui indique si les listes collées seront fusionnées avec les listes environnantes. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_MergePastedLists() const
```


## Exemples



Montre comment fusionner des listes à partir d'un document.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_MergePastedLists(true);

// Définissez la propriété "MergePastedLists" sur "true" ; les listes collées seront fusionnées avec les listes environnantes.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

dstDoc->Save(get_ArtifactsDir() + u"Document.MergePastedLists.docx");
```

## Voir aussi

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
