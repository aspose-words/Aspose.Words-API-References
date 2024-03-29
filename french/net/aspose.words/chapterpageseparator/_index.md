---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words pour .NET
description: Aspose.Words.ChapterPageSeparator énumération. Définit le caractère séparateur qui apparaît entre le chapitre et le numéro de page en C#.
type: docs
weight: 200
url: /fr/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

Définit le caractère séparateur qui apparaît entre le chapitre et le numéro de page.

```csharp
public enum ChapterPageSeparator
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Hyphen | `0` | Un deux-points. |
| Period | `1` | Un point. |
| Colon | `2` | Un deux-points. |
| EmDash | `3` | Un tiret accentué. |
| EnDash | `4` | Un tiret standard. |

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

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
