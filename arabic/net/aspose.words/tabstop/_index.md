---
title: Class TabStop
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.TabStop فصل. يمثل علامة تبويب مخصصة واحدة. الTabStopالكائن عضو في the TabStopCollection المجموعة.
type: docs
weight: 6200
url: /ar/net/aspose.words/tabstop/
---
## TabStop class

يمثل علامة تبويب مخصصة واحدة. ال`TabStop`الكائن عضو في the [`TabStopCollection`](../tabstopcollection/) المجموعة.

لمعرفة المزيد، قم بزيارة[نموذج كائن مستند Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public sealed class TabStop
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [TabStop](tabstop/#constructor)(double) | تهيئة مثيل جديد لهذه الفئة. |
| [TabStop](tabstop/#constructor_1)(double, TabAlignment, TabLeader) | تهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | الحصول على أو تعيين محاذاة النص عند علامة التبويب هذه. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | إرجاع`حقيقي` إذا قامت علامة التبويب هذه بمسح أي علامات جدولة موجودة في هذا الموضع. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | الحصول على أو تعيين نوع السطر الرئيسي المعروض أسفل حرف علامة التبويب. |
| [Position](../../aspose.words/tabstop/position/) { get; } | الحصول على موضع علامة التبويب بالنقاط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(TabStop) | يقارن مع المحدد`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | حساب رمز التجزئة لهذا الكائن. |

### ملاحظات

عادةً، تحدد علامة الجدولة الموضع الذي توجد فيه علامة الجدولة. ولكن نظرًا لأنه يمكن وراثة علامات الجدولة من الأنماط الأصلية، فقد يكون من الضروري أن يحدد الكائن التابع object بشكل صريح أنه لا توجد علامة جدولة في موضع معين. لمسح علامة جدولة موروثة عند موضع معين، قم بإنشاء ملف`TabStop` الكائن وset [`Alignment`](./alignment/) لClear.

لمزيد من المعلومات، راجع[`TabStopCollection`](../tabstopcollection/).

### أمثلة

يوضح كيفية تعديل موضع علامة التبويب اليمنى في الفقرات ذات الصلة بجدول المحتويات.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// التكرار خلال جميع الفقرات باستخدام أنماط جدول المحتويات المستندة إلى النتائج; هذا هو أي نمط بين TOC وTOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // احصل على علامة التبويب الأولى المستخدمة في هذه الفقرة، ويجب أن تكون هذه هي علامة التبويب المستخدمة لمحاذاة أرقام الصفحات.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // استبدل علامة التبويب الافتراضية الأولى، وتوقف بعلامة جدولة مخصصة.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


