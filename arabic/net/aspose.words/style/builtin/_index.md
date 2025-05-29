---
title: Style.BuiltIn
linktitle: BuiltIn
articleTitle: BuiltIn
second_title: Aspose.Words لـ .NET
description: اكتشف إن كان النمط مُدمجًا في مايكروسوفت وورد. حسّن تصميم مستندك مع دليلنا الشامل للأنماط المُدمجة في وورد!
type: docs
weight: 40
url: /ar/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

صحيح إذا كان هذا النمط أحد الأنماط المضمنة في MS Word.

```csharp
public bool BuiltIn { get; }
```

## أمثلة

يوضح كيفية التمييز بين الأنماط المخصصة والأنماط المضمنة.

```csharp
Document doc = new Document();

// عندما نقوم بإنشاء مستند باستخدام Microsoft Word، أو برمجيًا باستخدام Aspose.Words،
//ستأتي الوثيقة مع مجموعة من الأنماط لتطبيقها على النص لتعديل مظهره.
//يمكننا الوصول إلى هذه الأنماط المضمنة عبر مجموعة "الأنماط" الموجودة في المستند.
// ستحتوي جميع هذه الأنماط على علامة "مضمنة" مضبوطة على "صحيح".
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// إنشاء نمط مخصص وإضافته إلى المجموعة.
 // سيتم تعيين علامة "المدمج" إلى "خطأ" للأنماط المخصصة مثل هذا.
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### أنظر أيضا

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
