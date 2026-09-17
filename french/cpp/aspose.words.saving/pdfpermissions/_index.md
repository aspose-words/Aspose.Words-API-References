---
title: "Aspose::Words::Saving::PdfPermissions enum"
linktitle: "PdfPermissions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfPermissions enum. Spécifie les opérations autorisées pour un utilisateur sur un document PDF chiffré en C++."
type: docs
weight: 80000
url: /fr/cpp/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enum


Spécifie les opérations autorisées à un utilisateur sur un document PDF chiffré.

```cpp
enum class PdfPermissions
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| DisallowAll | 0 | Interdit toutes les opérations sur le document PDF. C’est la valeur par défaut. |
| AllowAll | 65535 | Autorise toutes les opérations sur le document PDF. |
| ContentCopy | n/a | Copier ou extraire autrement le texte et les graphiques du document par des opérations autres que celles contrôlées par [ContentCopyForAccessibility](./). |
| ContentCopyForAccessibility | n/a | Extraire le texte et les graphiques (dans le cadre de l’accessibilité pour les utilisateurs en situation de handicap ou à d’autres fins). |
| ModifyContents | n/a | Modifier le contenu du document par des opérations autres que celles contrôlées par [ModifyAnnotations](./), [FillIn](./) et [DocumentAssembly](./). |
| ModifyAnnotations | n/a | Ajouter ou modifier des annotations de texte, remplir des champs de formulaire interactifs et, si [ModifyContents](./) est également activé, créer ou modifier des champs de formulaire interactifs (y compris les champs de signature). |
| FillIn | n/a | Remplir les champs de formulaire interactifs existants (y compris les champs de signature), même si [ModifyContents](./) n’est pas activé. |
| DocumentAssembly | n/a | Assembler le document (insérer, faire pivoter ou supprimer des pages et créer des éléments de plan du document ou des images miniatures), même si [ModifyContents](./) n’est pas activé. |
| Printing | n/a | Imprimer le document (possiblement pas au niveau de qualité le plus élevé, selon que [HighResolutionPrinting](./) soit également activé). |
| HighResolutionPrinting | n/a | Imprimer le document sous une représentation à partir de laquelle une copie numérique fidèle du contenu PDF pourrait être générée, selon un algorithme dépendant de l’implémentation. Lorsque ce drapeau n’est pas activé (et que [Printing](./) est activé), l’impression doit être limitée à une représentation de bas niveau de l’apparence, éventuellement de qualité dégradée. |

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
