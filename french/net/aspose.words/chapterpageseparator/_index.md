---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.ChapterPageSeparator pour personnaliser les séparateurs de numéros de chapitre et de page pour une mise en forme et une clarté améliorées du document.
type: docs
weight: 390
url: /fr/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

Définit le caractère séparateur qui apparaît entre le numéro de chapitre et le numéro de page.

```csharp
public enum ChapterPageSeparator
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Hyphen | `0` | Deux points. |
| Period | `1` | Un point. |
| Colon | `2` | Deux points. |
| EmDash | `3` | Un tiret accentué. |
| EnDash | `4` | Un tableau de bord standard. |

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

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
