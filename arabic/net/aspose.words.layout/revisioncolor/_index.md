---
title: RevisionColor Enum
linktitle: RevisionColor
articleTitle: RevisionColor
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Layout.RevisionColor لتخصيص ألوان مراجعة المستندات، مما يعزز الوضوح ويحسن التعاون في مستنداتك.
type: docs
weight: 3830
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
| Auto | `0` | افتراضيًا. |
| Black | `1` | يمثل 000000 لون. |
| Blue | `2` | يمثل اللون 2e97d3. |
| BrightGreen | `3` | يمثل اللون 84a35b. |
| ClassicBlue | `4` | يمثل اللون 0000ff. |
| ClassicRed | `5` | يمثل لون ff0000. |
| DarkBlue | `6` | يمثل اللون 376e96. |
| DarkRed | `7` | يمثل 881824 لونًا. |
| DarkYellow | `8` | يمثل لون e09a2b. |
| Gray25 | `9` | يمثل اللون a0a3a9. |
| Gray50 | `10` | يمثل اللون 50565e. |
| Green | `11` | يمثل اللون 2c6234. |
| Pink | `12` | يمثل لون ce338f. |
| Red | `13` | يمثل لون b5082e. |
| Teal | `14` | يمثل لون 1b9cab. |
| Turquoise | `15` | يمثل لون 3eafc2. |
| Violet | `16` | يمثل 633277 لونًا. |
| White | `17` | يمثل اللون ffffff. |
| Yellow | `18` | يمثل لون fad272. |
| LightPink | `19` | يمثل لون fce6f4. |
| LightBlue | `20` | يمثل لون e1f2fa. |
| LightYellow | `21` | يمثل لون fef4de. |
| LightPurple | `22` | يمثل لون eadfef. |
| LightOrange | `23` | يمثل لون fce3d0. |
| LightGreen | `24` | يمثل اللون e9f8ce. |
| Gray | `25` | يمثل اللون المحدد. |
| NoHighlight | `26` | لا يتم استخدام أي لون لتسليط الضوء على تغييرات المراجعة. |
| ByAuthor | `27` | تتلقى مراجعات كل مؤلف لونًا خاصًا بها لتسليط الضوء عليه من مجموعة محددة مسبقًا من الألوان عالية التباين. |

## أمثلة

يوضح كيفية تغيير مظهر المراجعات في مستند الإخراج المقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أدرج مراجعة، ثم قم بتغيير لون جميع المراجعات إلى اللون الأخضر.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// قم بإزالة الشريط الذي يظهر على يسار كل سطر تمت مراجعته.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
