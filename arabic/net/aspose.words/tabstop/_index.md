---
title: TabStop
second_title: Aspose.Words لمراجع .NET API
description: يمثل علامة تبويب مخصصة واحدة. ال إيقاف التبويب الكائن هو عضو في TabStopCollection./tabstopcollection جمع .
type: docs
weight: 5900
url: /ar/net/aspose.words/tabstop/
---
## TabStop class

يمثل علامة تبويب مخصصة واحدة. ال **إيقاف التبويب** الكائن هو عضو في [`TabStopCollection`](../tabstopcollection) جمع .

```csharp
public sealed class TabStop
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [TabStop](tabstop#constructor)(double) | تهيئة مثيل جديد لهذه الفئة. |
| [TabStop](tabstop#constructor_1)(double, TabAlignment, TabLeader) | تهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment) { get; set; } | الحصول على محاذاة النص في علامة التبويب هذه أو تعيينها. |
| [IsClear](../../aspose.words/tabstop/isclear) { get; } | إرجاع صحيح إذا قامت علامة التبويب هذه بمسح أي توقفات علامة تبويب موجودة في هذا الموضع. |
| [Leader](../../aspose.words/tabstop/leader) { get; set; } | الحصول على أو تحديد نوع الخط الرئيسي المعروض أسفل حرف الجدولة. |
| [Position](../../aspose.words/tabstop/position) { get; } | يحصل على موضع علامة الجدولة بالنقاط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals#equals)(TabStop) | يقارن مع TabStop المحدد . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode)() | حساب كود التجزئة لهذا الكائن. |

### ملاحظات

عادةً ، تحدد علامة الجدولة موضعًا حيث توجد علامة الجدولة. ولكن نظرًا لأنه يمكن وراثة توقفات الجدولة من الأنماط الأصلية ، فقد يكون من الضروري أن يحدد الكائن الفرعي object بوضوح عدم وجود علامة جدولة في موضع معين. لمسح علامة الجدولة الموروثة في موضع معين ، قم بإنشاء ملف **إيقاف التبويب** الكائن و set [`Alignment`](./alignment) إلى`محاذاة الجدولة واضح`.

لمزيد من المعلومات، راجع[`TabStopCollection`](../tabstopcollection).

### أمثلة

يوضح كيفية تعديل موضع علامة الجدولة اليمنى في الفقرات المتعلقة بجداول المحتويات.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// التكرار خلال جميع الفقرات باستخدام الأنماط القائمة على جدول المحتويات ; هذا هو أي نمط بين TOC و TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // احصل على أول علامة تبويب مستخدمة في هذه الفقرة ، يجب أن تكون هذه هي علامة التبويب المستخدمة لمحاذاة أرقام الصفحات.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // استبدل أول علامة تبويب افتراضية ، توقف بعلامة جدولة مخصصة.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
