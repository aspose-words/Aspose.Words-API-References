---
title: Font.NameAscii
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. إرجاع أو تعيين الخط المستخدم للنص اللاتيني الأحرف ذات رموز الأحرف من 0 صفر إلى 127.
type: docs
weight: 240
url: /ar/net/aspose.words/font/nameascii/
---
## Font.NameAscii property

إرجاع أو تعيين الخط المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127).

```csharp
public string NameAscii { get; set; }
```

### أمثلة

يوضح كيف يمكن لـ Microsoft Word الجمع بين خطين مختلفين في تشغيل واحد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// لنفترض أن عملية التشغيل استخدمنا المنشئ لإدراجها أثناء استخدام تكوين الخط هذا
// يحتوي على أحرف ضمن نطاق أحرف ASCII. في هذه الحالة،
// سيتم عرض تلك الأحرف باستخدام هذا الخط.
builder.Font.NameAscii = "Calibri";

// مع عدم تحديد خط آخر، سيقوم المنشئ أيضًا بتطبيق هذا الخط على جميع الأحرف التي يقوم بإدراجها.
Assert.AreEqual("Calibri", builder.Font.Name);

// حدد خطًا لاستخدامه لجميع الأحرف خارج نطاق ASCII.
// من الناحية المثالية، يجب أن يحتوي هذا الخط على حرف رسومي لكل رمز حرف غير ASCII مطلوب.
builder.Font.NameOther = "Courier New";

// أدخل تشغيلًا يحتوي على كلمة واحدة تتكون من أحرف ASCII، وكلمة واحدة تحتوي على جميع الأحرف خارج هذا النطاق.
// سيتم عرض كل حرف باستخدام أي من الخطوط، اعتمادًا على ذلك.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### أنظر أيضا

* property [Name](../name/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


