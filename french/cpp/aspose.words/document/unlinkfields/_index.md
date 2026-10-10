---
title: "Aspose::Words::Document::UnlinkFields méthode"
linktitle: "UnlinkFields"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::UnlinkFields méthode. Dissocie les champs dans l'ensemble du document en C++."
type: docs
weight: 94000
url: /fr/cpp/aspose.words/document/unlinkfields/
---
## Document::UnlinkFields method


Délie les champs dans l'ensemble du document.

```cpp
void Aspose::Words::Document::UnlinkFields()
```

## Remarques


Remplace tous les champs de l'ensemble du document par leurs résultats les plus récents.

Pour dissocier les champs dans une partie spécifique du document, utilisez [UnlinkFields](../../range/unlinkfields/).

## Exemples



Montre comment dissocier tous les champs du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

doc->UnlinkFields();
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
