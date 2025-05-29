---
title: FieldIndexFormat Enum
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.FieldIndexFormat لتنسيق FieldIndex القابل للتخصيص في مستنداتك. حسّن بنية مستندك بسهولة!
type: docs
weight: 2480
url: /ar/net/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enumeration

يحدد التنسيق لـ[`FieldIndex`](../fieldindex/) الحقول في المستند.

```csharp
public enum FieldIndexFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Template | `0` | من القالب. |
| Classic | `1` | كلاسيكي. |
| Fancy | `2` | باهِظ. |
| Modern | `3` | حديث. |
| Bulleted | `4` | نقطية. |
| Formal | `5` | رَسمِيّ. |
| Simple | `6` | بسيط. |

## أمثلة

يوضح كيفية تنسيق حقول FieldIndex.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("A");
builder.InsertBreak(BreakType.LineBreak);
builder.InsertField("XE \"A\"");
builder.Write("B");

builder.InsertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

doc.FieldOptions.FieldIndexFormat = FieldIndexFormat.Fancy;
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.SetFieldIndexFormat.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
