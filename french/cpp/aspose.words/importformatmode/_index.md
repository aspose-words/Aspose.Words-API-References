---
title: "Enum Aspose::Words::ImportFormatMode"
linktitle: "ImportFormatMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Enum Aspose::Words::ImportFormatMode. Spécifie comment le formatage est fusionné lors de l'importation de contenu depuis un autre document en C++."
type: docs
weight: 93000
url: /fr/cpp/aspose.words/importformatmode/
---
## ImportFormatMode enum


Spécifie comment la mise en forme est fusionnée lors de l'importation de contenu depuis un autre document.

```cpp
enum class ImportFormatMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| UseDestinationStyles | 0 | Utilise les styles du document de destination et copie les nouveaux styles. C'est l'option par défaut. |
| KeepSourceFormatting | 1 | Copie tous les styles requis dans le document de destination, génère des noms de style uniques si nécessaire. |
| KeepDifferentStyles | 2 | Copiez uniquement les styles qui diffèrent de ceux du document source. |

## Remarques


Lorsque vous copiez des nœuds d'un document à un autre, cette option spécifie comment le formatage est résolu lorsque les deux documents ont un style portant le même nom, mais un formatage différent.

Le formatage est résolu comme suit :

1. Les styles intégrés sont associés à l'aide de leur identifiant de style indépendant de la langue. Les styles définis par l'utilisateur sont associés à l'aide du nom de style sensible à la casse.
1. Si aucun style correspondant n'est trouvé dans le document de destination, le style (et tous les styles qui y font référence) sont copiés dans le document de destination et les nœuds importés sont mis à jour pour référencer le nouveau style.
1. Si un style correspondant existe déjà dans le document de destination, le résultat dépend du paramètre **importFormatMode** passé à [ImportNode()](../) comme décrit ci‑dessous.



Lors de l'utilisation de l'option [UseDestinationStyles](./), si un style correspondant existe déjà dans le document de destination, le style n'est pas copié et les nœuds importés sont mis à jour pour référencer le style existant.

L'inconvénient d'utiliser [UseDestinationStyles](./) est que le texte importé peut apparaître différemment dans le document de destination par rapport au document source. Par exemple, le style \"Heading 1\" du document source utilise la police Arial 16 pt et le style \"Heading 1\" du document de destination utilise la police Times New Roman 14 pt. Lors de l'importation de texte avec le style \"Heading 1\" sans autre formatage direct, il apparaîtra en Times New Roman 14 pt dans le document de destination.

[KeepSourceFormatting](./) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct [Node](../node/) attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct [Node](../node/) attributes in favor of preserving original [Node](../node/) formatting.

L'inconvénient d'utiliser [KeepSourceFormatting](./) est que si vous effectuez plusieurs importations, vous pourriez vous retrouver avec de nombreux styles dans le document de destination, ce qui peut rendre difficile l'utilisation d'un formatage de style cohérent dans Microsoft Word pour ce document.

Utiliser l'option [KeepDifferentStyles](./) permet de réutiliser les styles de destination si le formatage qu'ils offrent est identique à celui des styles du document source. Si le style dans le document de destination diffère de celui du source, il est alors importé.

## Exemples



Montre comment insérer un document dans un autre document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

auto docToInsert = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Formatted elements.docx");

builder->InsertDocument(docToInsert, Aspose::Words::ImportFormatMode::KeepSourceFormatting);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocument.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
