---
title: DocumentBase.Lists
second_title: Aspose.Words لمراجع .NET API
description: DocumentBase ملكية. يوفر الوصول إلى تنسيق القائمة المستخدم في المستند.
type: docs
weight: 40
url: /ar/net/aspose.words/documentbase/lists/
---
## DocumentBase.Lists property

يوفر الوصول إلى تنسيق القائمة المستخدم في المستند.

```csharp
public ListCollection Lists { get; }
```

### ملاحظات

لمزيد من المعلومات راجع وصف[`ListCollection`](../../../aspose.words.lists/listcollection/) فصل.

### أمثلة

يوضح كيفية العمل مع مستويات القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز البادئة والمسافات البادئة.
 // يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا بدء القائمة وإنهائها باستخدام خاصية "ListFormat" الخاصة بمنشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// فيما يلي نوعان من القوائم التي يمكننا إنشاؤها باستخدام أداة إنشاء المستندات.
// 1 - قائمة مرقمة:
// تنشئ القوائم المرقمة ترتيبًا منطقيًا لفقراتها عن طريق ترقيم كل عنصر.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// من خلال تعيين خاصية "ListLevelNumber"، يمكننا زيادة مستوى القائمة
// لبدء قائمة فرعية قائمة بذاتها في عنصر القائمة الحالي.
// يستخدم قالب قائمة Microsoft Word المسمى "NumberDefault" الأرقام لإنشاء مستويات القائمة لمستوى القائمة الأول.
 // تستخدم مستويات القائمة الأعمق الحروف والأرقام الرومانية الصغيرة.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - قائمة ذات تعداد نقطي:
// ستطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
// ستستخدم المستويات الأعمق لهذه القائمة رموزًا مختلفة، مثل "■" و"○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// يمكننا تعطيل تنسيق القائمة لعدم تنسيق أي فقرات لاحقة كقوائم عن طريق إلغاء تعيين علامة "القائمة".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### أنظر أيضا

* class [ListCollection](../../../aspose.words.lists/listcollection/)
* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../documentbase/)
* المجسم [Aspose.Words](../../../)


