---
title: Font.NameOther
linktitle: NameOther
articleTitle: NameOther
second_title: Aspose.Words لـ .NET
description: اكتشف اسم الخط. خصّص الخطوط بسهولة لرموز الأحرف من ١٢٨ إلى ٢٥٥، مما يُحسّن أسلوب نصك وسهولة قراءته. ارتقِ بتصميمك اليوم!
type: docs
weight: 270
url: /ar/net/aspose.words/font/nameother/
---
## Font.NameOther property

يعيد أو يضبط الخط المستخدم للأحرف التي تحتوي على رموز أحرف من 128 إلى 255.

```csharp
public string NameOther { get; set; }
```

## أمثلة

يوضح كيف يمكن لبرنامج Microsoft Word دمج خطين مختلفين في تشغيل واحد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// افترض تشغيلًا نستخدم فيه المنشئ للإدراج أثناء استخدام تكوين الخط هذا
// يحتوي على أحرف ضمن نطاق أحرف ASCII. في هذه الحالة،
//سيتم عرض تلك الأحرف باستخدام هذا الخط.
builder.Font.NameAscii = "Calibri";

// في حالة عدم تحديد أي خط آخر، سيقوم المنشئ أيضًا بتطبيق هذا الخط على جميع الأحرف التي يقوم بإدراجها.
Assert.AreEqual("Calibri", builder.Font.Name);

// حدد الخط الذي سيتم استخدامه لجميع الأحرف خارج نطاق ASCII.
// من الناحية المثالية، ينبغي أن يحتوي هذا الخط على رمز لكل رمز حرف غير ASCII مطلوب.
builder.Font.NameOther = "Courier New";

// قم بإدراج تشغيل بكلمة واحدة تتكون من أحرف ASCII، وكلمة واحدة تحتوي على جميع الأحرف خارج هذا النطاق.
//سيتم عرض كل حرف باستخدام أحد الخطوط، اعتمادًا على.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### أنظر أيضا

* property [Name](../name/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
