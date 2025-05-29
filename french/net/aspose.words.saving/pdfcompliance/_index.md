---
title: PdfCompliance Enum
linktitle: PdfCompliance
articleTitle: PdfCompliance
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Saving.PdfCompliance pour améliorer la conformité de vos documents PDF. Améliorez la qualité de vos documents grâce à des options sur mesure pour chaque besoin !
type: docs
weight: 6200
url: /fr/net/aspose.words.saving/pdfcompliance/
---
## PdfCompliance enumeration

Spécifie le niveau de conformité aux normes PDF.

```csharp
public enum PdfCompliance
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Pdf17 | `0` | Le fichier de sortie sera conforme à la norme PDF 1.7 (ISO 32000-1). |
| Pdf20 | `1` | Le fichier de sortie sera conforme à la norme PDF 2.0 (ISO 32000-2). |
| PdfA1a | `2` | Le fichier de sortie sera conforme à la norme PDF/A-1a (ISO 19005-1). Ce niveau inclut toutes les exigences de la norme PDF/A-1b et exige en outre que la structure du document soit incluse (également appelée « balisage »), dans le but de garantir que le contenu du document puisse être recherché et réutilisé. |
| PdfA1b | `3` | Le fichier de sortie sera conforme à la norme PDF/A-1b (ISO 19005-1). PDF/A-1b a pour objectif d'assurer une reproduction fiable de l' apparence visuelle du document. |
| PdfA2a | `4` | Le fichier de sortie sera conforme à la norme PDF/A-2a (ISO 19005-2). Ce niveau inclut toutes les exigences de PDF/A-2u et exige en outre que la structure du document soit incluse (également appelée « balisage »), dans le but de garantir que le contenu du document puisse être recherché et réutilisé. |
| PdfA2u | `5` | Le fichier de sortie sera conforme à la norme PDF/A-2u (ISO 19005-2). PDF/A-2u vise à préserver l'aspect visuel statique du document au fil du temps, indépendamment des outils et systèmes utilisés pour créer, stocker ou afficher les fichiers. De plus, tout texte contenu dans le document peut être extrait de manière fiable sous forme de points de code Unicode. |
| PdfA3a | `6` | Le fichier de sortie sera conforme à la norme PDF/A-3a (ISO 19005-3). Ce niveau inclut toutes les exigences de la norme PDF/A-3u et exige en outre que la structure du document soit incluse (également appelée « balisage »), dans le but de garantir que le contenu du document puisse être recherché et réutilisé. |
| PdfA3u | `7` | Le fichier de sortie sera conforme à la norme PDF/A-3u (ISO 19005-3). PDF/A-3u (et PDF/A-2u) a pour objectif de préserver l'aspect visuel statique du document au fil du temps, indépendamment des outils et systèmes utilisés pour créer, stocker ou afficher les fichiers. De plus, tout texte contenu dans le document peut être extrait de manière fiable sous forme de points de code Unicode. Outre PDF/A-2u, PDF/A-3u permet l'intégration de pièces jointes au document PDF. |
| PdfA4 | `8` | Le fichier de sortie sera conforme à la norme PDF/A-4 (ISO 19005-4:2020). PDF/A-4 vise à préserver l'aspect visuel statique du document au fil du temps, indépendamment des outils et systèmes utilisés pour créer, stocker ou afficher les fichiers. De plus, tout texte contenu dans le document peut être extrait de manière fiable sous forme de points de code Unicode. |
| PdfA4f | `9` | Le fichier de sortie sera conforme à la norme PDF/A-4f (ISO 19005-4:2020). Ce niveau inclut toutes les exigences de PDF/A-4 et permet en outre l'intégration de pièces jointes au document PDF. |
| PdfA4Ua2 | `10` | Le fichier de sortie sera conforme aux normes PDF/A-4 (ISO 19005-4:2020) et PDF/UA-2 (ISO 14289-2:2024). PDF/A-4 a pour objectif de préserver l'aspect visuel statique des documents au fil du temps, indépendamment des outils et systèmes utilisés pour créer, stocker ou afficher les fichiers. L'objectif principal de PDF/UA est de définir comment représenter les documents électroniques au format PDF de manière à ce qu'ils soient accessibles. |
| PdfUa1 | `11` | Le fichier de sortie sera conforme à la norme PDF/UA-1 (ISO 14289-1). L'objectif principal de PDF/UA est de définir comment représenter les documents électroniques au format PDF d'une manière qui permette au fichier d'être accessible. |
| PdfUa2 | `12` | Le fichier de sortie sera conforme à la norme PDF/UA-2 (ISO 14289-2:2024). L'objectif principal de PDF/UA est de définir comment représenter les documents électroniques au format PDF d'une manière qui permette au fichier d'être accessible. |

## Exemples

Montre comment définir le niveau de conformité aux normes PDF des documents PDF enregistrés.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
// Notez que certaines options PdfSaveOptions sont interdites lors de l'enregistrement selon l'une des normes et automatiquement corrigées.
// Utilisez IWarningCallback pour savoir quelles options sont automatiquement corrigées.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Définissez la propriété « Compliance » sur « PdfCompliance.PdfA1b » pour être conforme à la norme « PDF/A-1b »,
// qui vise à préserver l'apparence visuelle du document pendant qu'Aspose.Words le convertit en PDF.
// Définissez la propriété « Compliance » sur « PdfCompliance.Pdf17 » pour être conforme à la norme « 1.7 ».
// Définissez la propriété « Compliance » sur « PdfCompliance.PdfA1a » pour être conforme à la norme « PDF/A-1a »,
// qui est conforme à la norme « PDF/A-1b » tout en préservant la structure du document d'origine.
// Définissez la propriété « Compliance » sur « PdfCompliance.PdfUa1 » pour être conforme à la norme « PDF/UA-1 » (ISO 14289-1),
// qui vise à définir les documents électroniques représentés en PDF qui permettent de rendre le fichier accessible.
// Définissez la propriété « Compliance » sur « PdfCompliance.Pdf20 » pour être conforme à la norme « PDF 2.0 » (ISO 32000-2).
// Définissez la propriété « Compliance » sur « PdfCompliance.PdfA4 » pour être conforme à la norme « PDF/A-4 » (ISO 19004:2020),
// qui préserve l'apparence visuelle statique du document au fil du temps.
// Définissez la propriété « Compliance » sur « PdfCompliance.PdfA4Ua2 » pour être conforme à la norme PDF/A-4 (ISO 19005-4:2020)
// et les normes PDF/UA-2 (ISO 14289-2:2024).
// Définissez la propriété « Compliance » sur « PdfCompliance.PdfUa2 » pour être conforme à la norme PDF/UA-2 (ISO 14289-2:2024).
// Cela permet de rendre les documents consultables, mais peut augmenter considérablement la taille de documents déjà volumineux.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
