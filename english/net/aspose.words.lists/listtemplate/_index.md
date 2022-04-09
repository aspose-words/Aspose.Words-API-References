---
title: ListTemplate
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 3270
url: /net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

Specifies one of the predefined list formats available in Microsoft Word.

```csharp
public enum ListTemplate
```

## Values

| name | value | description |
| --- | --- | --- |
| BulletDefault | `0` | Default bulleted list with 9 levels. Bullet of the first level is a disc, bullet of the second level is a circle, bullet of the third level is a square. Then formatting repeats for the remaining levels.Each level is indented to the right by 0.25" relative to the previous level.Corresponds to the 1st bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletDisk | `0` | Same as BulletDefault.Corresponds to the 1st bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletCircle | `1` | The bullet of the first level is a circle. The remaining levels are same as in BulletDefault.Corresponds to the 2nd bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletSquare | `2` | The bullet of the first level is a square. The remaining levels are same as in BulletDefault.Corresponds to the 3rd bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletDiamonds | `3` | The bullet of the first level is a 4-diamond Wingding character. The remaining levels are same as in BulletDefault.Corresponds to the 5th bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletArrowHead | `4` | The bullet of the first level is an arrow head Wingding character. The remaining levels are same as in BulletDefault.Corresponds to the 6th bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| BulletTick | `5` | The bullet of the first level is a tick Wingding character. The remaining levels are same as in BulletDefault.Corresponds to the 7th bulleted list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberDefault | `6` | Default numbered list with 9 levels. Arabic numbering (1., 2., 3., ...) for the first level, lowercase letter numbering (a., b., c., ...) for the second level, lowercase roman numbering (i., ii., iii., ...) for the third level. Then formatting repeats for the remaining levels.Each level is indented to the right by 0.25" relative to the previous level.Corresponds to the 1st numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberArabicDot | `6` | Same as NumberDefault.Corresponds to the 1st numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberArabicParenthesis | `7` | The number of the first level is "1)". The remaining levels are same as in NumberDefault.Corresponds to the 2nd numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberUppercaseRomanDot | `8` | The number of the first level is "I.". The remaining levels are same as in NumberDefault.Corresponds to the 3rd numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberUppercaseLetterDot | `9` | The number of the first level is "A.". The remaining levels are same as in NumberDefault.Corresponds to the 4th numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberLowercaseLetterParenthesis | `10` | The number of the first level is "a)". The remaining levels are same as in NumberDefault.Corresponds to the 5th numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberLowercaseLetterDot | `11` | The number of the first level is "a.". The remaining levels are same as in NumberDefault.Corresponds to the 6th numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| NumberLowercaseRomanDot | `12` | The number of the first level is "i.". The remaining levels are same as in NumberDefault.Corresponds to the 7th numbered list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineNumbers | `13` | An outline list with levels numbered "1), a), i), (1), (a), (i), 1., a., i.".Corresponds to the 1st outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineLegal | `14` | An outline list with levels are numbered "1., 1.1., 1.1.1, ...".Corresponds to the 2nd outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineBullets | `15` | An outline lists with various bullets for different levels.Corresponds to the 3rd outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineHeadingsArticleSection | `16` | An outline list with levels linked to Heading styles.Corresponds to the 4th outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineHeadingsLegal | `17` | An outline list with levels linked to Heading styles.Corresponds to the 5th outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineHeadingsNumbers | `18` | An outline list with levels linked to Heading styles.Corresponds to the 6th outline list template in the Bullets and Numbering dialog box in Microsoft Word. |
| OutlineHeadingsChapter | `19` | An outline list with levels linked to Heading styles.Corresponds to the 7th outline list template in the Bullets and Numbering dialog box in Microsoft Word. |

## Remarks

A list template value is used as a parameter into the [`Add`](../listcollection/add) method.Aspose.Words list templates correspond to the 21 list templates available in the Bullets and Numbering dialog box in Microsoft Word 2003.

### See Also

* namespace [Aspose.Words.Lists](../../aspose.words.lists)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
