---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words pour .NET
description: PageSetup ChapterPageSeparator propriété. Obtient ou définit le caractère séparateur qui apparaît entre le numéro de chapitre et le numéro de page en C#.
type: docs
weight: 90
url: /fr/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

Obtient ou définit le caractère séparateur qui apparaît entre le numéro de chapitre et le numéro de page.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

## Remarques

Avant de pouvoir créer des numéros de page incluant des numéros de chapitre, les titres du document doivent avoir un format de plan numéroté appliqué.

## Exemples

Montre comment travailler avec les chapitres de page.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### Voir également

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
