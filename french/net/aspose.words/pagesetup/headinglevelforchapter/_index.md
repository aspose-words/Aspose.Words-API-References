---
title: PageSetup.HeadingLevelForChapter
linktitle: HeadingLevelForChapter
articleTitle: HeadingLevelForChapter
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup HeadingLevelForChapter pour personnaliser facilement les styles de titre de chapitre dans votre document pour une lisibilité et un professionnalisme améliorés.
type: docs
weight: 180
url: /fr/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Obtient ou définit le style de niveau de titre appliqué aux titres de chapitre dans le document.

```csharp
public int HeadingLevelForChapter { get; set; }
```

## Remarques

Peut être un nombre compris entre 0 et 9. 0 signifie qu'il n'y a pas de numéro de chapitre s'il est appliqué au numéro de page.

Avant de pouvoir créer des numéros de page incluant des numéros de chapitre, les titres du document doivent avoir un format de plan numéroté appliqué.

## Exemples

Montre comment travailler avec des chapitres de page.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
