---
title: WarningSource Enum
linktitle: WarningSource
articleTitle: WarningSource
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.WarningSource, identifiant les sources d'avertissement lors du chargement et de l'enregistrement des documents pour une gestion améliorée des documents.
type: docs
weight: 7500
url: /fr/net/aspose.words/warningsource/
---
## WarningSource enumeration

Spécifie le module qui génère un avertissement lors du chargement ou de l'enregistrement du document.

```csharp
public enum WarningSource
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Unknown | `0` | La source de l'avertissement n'est pas spécifiée. |
| Layout | `1` | Module qui construit une mise en page de document. |
| DrawingML | `2` | Module qui rend les formes DrawingML. |
| OfficeMath | `3` | Module qui rend OfficeMath. |
| Shapes | `4` | Module qui rend les formes ordinaires. |
| Metafile | `5` | Module qui restitue les métafichiers. |
| Xps | `6` | Module qui rend XPS. |
| Pdf | `7` | Module qui rend le PDF. |
| Image | `8` | Module qui rend les images. |
| Docx | `9` | Module qui lit/écrit des fichiers DOCX. |
| Doc | `10` | Module qui lit/écrit des fichiers DOC binaires. |
| Text | `11` | Module qui lit/écrit des fichiers en texte brut. |
| Rtf | `12` | Module qui lit/écrit des fichiers RTF. |
| WordML | `13` | Module qui lit/écrit des fichiers WML. |
| Nrx | `14` | Modules communs partagés entre les modules de lecture/écriture DOCX/WML. |
| Odt | `15` | Module qui lit/écrit les fichiers ODT. |
| Html | `16` | Module qui lit/écrit des fichiers HTML/MHTML. |
| Validator | `17` | Module qui vérifie la cohérence et la validité du modèle. |
| Xaml | `18` | Module qui lit/écrit les fichiers Xaml. |
| Svm | `19` | Module qui lit les fichiers Svm. |
| MathML | `20` | Module qui lit les fichiers W3C MathML. |
| Font | `21` | Module qui lit les fichiers de polices. |
| Svg | `22` | Module qui lit les fichiers SVG. |
| Markdown | `23` | Module qui lit/écrit les fichiers Markdown. |
| Chm | `24` | Module qui lit les fichiers CHM. |
| Epub | `25` | Module qui lit/écrit les fichiers EPUB. |
| Xml | `26` | Module qui lit les fichiers XML. |
| Xlsx | `27` | Module qui écrit des fichiers XLSX. |

## Exemples

Montre comment travailler avec la source d'avertissement.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
