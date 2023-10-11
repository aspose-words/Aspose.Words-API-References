---
title: Style.BuiltIn
second_title: Aspose.Words لمراجع .NET API
description: Style ملكية. صحيح إذا كان هذا النمط أحد الأنماط المضمنة في برنامج MS Word.
type: docs
weight: 40
url: /ar/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

صحيح إذا كان هذا النمط أحد الأنماط المضمنة في برنامج MS Word.

```csharp
public bool BuiltIn { get; }
```

### أمثلة

يوضح كيفية التمييز بين الأنماط المخصصة والأنماط المضمنة.

```csharp
Document doc = new Document();

// عندما نقوم بإنشاء مستند باستخدام Microsoft Word، أو برمجيًا باستخدام Aspose.Words،
// ستأتي الوثيقة بمجموعة من الأنماط لتطبيقها على نصها لتعديل مظهرها.
// يمكننا الوصول إلى هذه الأنماط المضمنة عبر مجموعة "الأنماط" الخاصة بالمستند.
// ستحتوي جميع هذه الأنماط على علامة "BuiltIn" مضبوطة على "true".
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// أنشئ نمطًا مخصصًا وأضفه إلى المجموعة.
// الأنماط المخصصة مثل هذه ستحتوي على علامة "BuiltIn" مضبوطة على "خطأ".
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### أنظر أيضا

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../style/)
* المجسم [Aspose.Words](../../../)


