---
title: RevisionColor Enum
linktitle: RevisionColor
articleTitle: RevisionColor
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Layout.RevisionColor تعداد. يسمح بتحديد لون مراجعات المستند في C#.
type: docs
weight: 3380
url: /ar/net/aspose.words.layout/revisioncolor/
---
## RevisionColor enumeration

يسمح بتحديد لون مراجعات المستند.

```csharp
public enum RevisionColor
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Auto | `0` | الافتراضي. |
| Black | `1` | يمثل 000000 لون. |
| Blue | `2` | يمثل اللون 2e97d3. |
| BrightGreen | `3` | يمثل اللون 84a35b. |
| ClassicBlue | `4` | يمثل اللون 0000ff. |
| ClassicRed | `5` | يمثل اللون ff0000. |
| DarkBlue | `6` | يمثل 376e96 لون. |
| DarkRed | `7` | يمثل 881824 لون. |
| DarkYellow | `8` | يمثل اللون e09a2b. |
| Gray25 | `9` | يمثل اللون a0a3a9. |
| Gray50 | `10` | يمثل لون 50565e. |
| Green | `11` | يمثل لون 2c6234. |
| Pink | `12` | يمثل اللون ce338f. |
| Red | `13` | يمثل اللون b5082e. |
| Teal | `14` | يمثل لون 1b9cab. |
| Turquoise | `15` | يمثل لون 3eafc2. |
| Violet | `16` | يمثل 633277 لون. |
| White | `17` | يمثل اللون ffffff. |
| Yellow | `18` | يمثل لونفاد272. |
| NoHighlight | `19` | لم يتم استخدام أي لون لتسليط الضوء على تغييرات المراجعة. |
| ByAuthor | `20` | تحصل مراجعات كل مؤلف على اللون الخاص بها لتسليط الضوء عليها من مجموعة محددة مسبقًا من الألوان عالية التباين. |

## أمثلة

يوضح كيفية تغيير مظهر المراجعات في مستند الإخراج المقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل مراجعة، ثم قم بتغيير لون كافة المراجعات إلى اللون الأخضر.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// قم بإزالة الشريط الذي يظهر على يسار كل سطر تمت مراجعته.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
