---
title: PageSetup.HeadingLevelForChapter
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Obtient ou définit le style de niveau de titre appliqué aux titres de chapitre dans le document.
type: docs
weight: 180
url: /fr/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Obtient ou définit le style de niveau de titre appliqué aux titres de chapitre dans le document.

```csharp
public int HeadingLevelForChapter { get; set; }
```

### Remarques

Peut être un nombre compris entre 0 et 9. 0 signifie aucun numéro de chapitre s’il est appliqué au numéro de page.

Avant de pouvoir créer des numéros de page incluant des numéros de chapitre, les titres du document doivent avoir un format de plan numéroté appliqué.

### Exemples

Montre comment travailler avec les chapitres de page.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


