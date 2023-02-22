---
title: Style.BuiltIn
second_title: Aspose.Words لمراجع .NET API
description: Style ملكية. صحيح إذا كان هذا النمط أحد الأنماط المضمنة في MS Word .
type: docs
weight: 30
url: /ar/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

صحيح إذا كان هذا النمط أحد الأنماط المضمنة في MS Word .

```csharp
public bool BuiltIn { get; }
```

### أمثلة

يوضح كيفية التمييز بين الأنماط المخصصة والأنماط المضمنة.

```csharp
Document doc = new Document();

// عندما ننشئ مستندًا باستخدام Microsoft Word ، أو باستخدام Aspose.Words برمجيًا ،
// سيأتي المستند مع مجموعة من الأنماط لتطبيقها على نصه لتعديل مظهره.
// يمكننا الوصول إلى هذه الأنماط المضمنة عبر مجموعة "Styles" الخاصة بالمستند.
// هذه الأنماط جميعها تحتوي على علامة "مضمّنة" مضبوطة على "صواب".
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// أنشئ نمطًا مخصصًا وأضفه إلى المجموعة.
 // الأنماط المخصصة مثل هذا سيتم تعيين علامة "مضمّنة" على "خطأ".
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### أنظر أيضا

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../style/)
* المجسم [Aspose.Words](../../../)


