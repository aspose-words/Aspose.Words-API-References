---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.DropCapPosition enum لتعزيز تصميم مستندك من خلال تحديد مواضع نص فريدة للأحرف الكبيرة المنسدلة للحصول على جاذبية بصرية مؤثرة.
type: docs
weight: 1820
url: /ar/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

يحدد موضع النص ذي الأحرف الكبيرة.

```csharp
public enum DropCapPosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | الفقرة لا تحتوي على حرف كبير. |
| Normal | `1` | يتم وضع الحرف الكبير داخل هامش النص في فقرة المرساة. |
| Margin | `2` | يتم وضع الحرف الكبير خارج هامش النص في فقرة المرساة. |

## أمثلة

يوضح كيفية إنشاء حرف كبير.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج فقرة واحدة بحرف كبير يبدأ به النص في الفقرتين الثانية والثالثة.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// حاليًا، ستظهر الفقرتان الثانية والثالثة أسفل الفقرة الأولى.
// يمكننا تحويل الفقرة الأولى إلى حرف كبير منسدل للفقرات الأخرى عبر كائن "ParagraphFormat" الخاص بها.
// اضبط خاصية "DropCapPosition" على "DropCapPosition.Margin" لوضع الحرف الكبير
// خارج هامش الصفحة الأيسر إذا كان النص من اليسار إلى اليمين.
// اضبط خاصية "DropCapPosition" على "DropCapPosition.Normal" لوضع الحرف الكبير داخل هوامش الصفحة
//ولتغليف بقية النص حوله.
//"DropCapPosition.None" هي الحالة الافتراضية لجميع الفقرات.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
