---
title: Enum DropCapPosition
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.DropCapPosition تعداد. يحدد موضع النص الاستهلالي .
type: docs
weight: 1260
url: /ar/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

يحدد موضع النص الاستهلالي .

```csharp
public enum DropCapPosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | الفقرة ليس لها حرف استهلالي . |
| Normal | `1` | يتم وضع الحرف الاستهلالي داخل هامش النص في فقرة الربط. |
| Margin | `2` | يتم وضع الحرف الاستهلالي خارج هامش النص في فقرة الربط. |

### أمثلة

يوضح كيفية إنشاء غطاء رأس منسدل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل فقرة واحدة بحرف كبير يبدأ به النص في الفقرتين الثانية والثالثة.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// حاليًا ، ستظهر الفقرتان الثانية والثالثة أسفل الأولى.
// يمكننا تحويل الفقرة الأولى كحرف استهلالي للفقرات الأخرى عبر كائن "تنسيق الفقرة".
// قم بتعيين خاصية "DropCapPosition" على "DropCapPosition.Margin" لوضع الأحرف الاستهلالية الكبيرة
// خارج هامش الصفحة الأيسر إذا كان النص من اليسار إلى اليمين.
// عيّن خاصية "DropCapPosition" على "DropCapPosition.Normal" لوضع الأحرف الاستهلالية الكبيرة داخل هوامش الصفحة
// ولف باقي النص حوله.
// "DropCapPosition.None" هي الحالة الافتراضية لجميع الفقرات.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


