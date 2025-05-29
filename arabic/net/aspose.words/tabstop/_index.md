---
title: TabStop Class
linktitle: TabStop
articleTitle: TabStop
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.TabStop، الحل الأمثل لعلامات تبويب مخصصة في تنسيق المستندات. حسّن مستنداتك بدقة وسهولة!
type: docs
weight: 7050
url: /ar/net/aspose.words/tabstop/
---
## TabStop class

يمثل علامة تبويب مخصصة واحدة.`TabStop` الكائن هو عضو في [`TabStopCollection`](../tabstopcollection/) المجموعة.

لمعرفة المزيد، قم بزيارة[نموذج كائن المستند (DOM) في Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public sealed class TabStop
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [TabStop](tabstop/#constructor)(*double*) | يقوم بتهيئة مثيل جديد لهذه الفئة. |
| [TabStop](tabstop/#constructor_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | يقوم بتهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | يحصل على محاذاة النص عند علامة التبويب هذه أو يعينها. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | إرجاع`حقيقي` إذا كانت علامة التبويب هذه تمسح أي علامات تبويب موجودة في هذا الموضع. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | يحصل على نوع الخط الرئيسي المعروض أسفل حرف التبويب أو يعينه. |
| [Position](../../aspose.words/tabstop/position/) { get; } | يحصل على موضع علامة التبويب بالنقاط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(*TabStop*) | يقارن مع المحدد`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | يحسب رمز التجزئة لهذا الكائن. |

## ملاحظات

عادةً، تُحدد علامة التبويب موضعًا توجد فيه. ولكن نظرًا لإمكانية توريث علامات التبويب من الأنماط الأصلية، فقد يلزم أن يُحدد الكائن الفرعي صراحةً عدم وجود علامة تبويب في موضع مُحدد. لمسح علامة تبويب موروثة في موضع مُحدد، أنشئ`TabStop` الكائن و set [`Alignment`](./alignment/) لClear.

لمزيد من المعلومات انظر[`TabStopCollection`](../tabstopcollection/).

## أمثلة

يوضح كيفية تعديل موضع علامة التبويب اليمنى في الفقرات ذات الصلة بجدول المحتويات.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// قم بالتكرار خلال جميع الفقرات باستخدام أنماط تعتمد على نتائج جدول المحتويات; وهذا هو أي نمط بين جدول المحتويات وجدول المحتويات 9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // احصل على علامة التبويب الأولى المستخدمة في هذه الفقرة، ويجب أن تكون هذه هي علامة التبويب المستخدمة لمحاذاة أرقام الصفحات.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // استبدال علامة التبويب الافتراضية الأولى، والتوقف بعلامة تبويب مخصصة.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
