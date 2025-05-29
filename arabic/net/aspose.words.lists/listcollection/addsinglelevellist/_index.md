---
title: ListCollection.AddSingleLevelList
linktitle: AddSingleLevelList
articleTitle: AddSingleLevelList
second_title: Aspose.Words لـ .NET
description: قم بإنشاء قائمة ذات مستوى واحد وإضافتها إلى مستندك بسهولة باستخدام طريقة AddSingleLevelList من ListCollection، مما يعمل على تحسين التنظيم والوضوح.
type: docs
weight: 60
url: /ar/net/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection.AddSingleLevelList method

ينشئ قائمة جديدة ذات مستوى واحد استنادًا إلى القالب المحدد مسبقًا ويضيفها إلى مجموعة القوائم في المستند.

```csharp
public List AddSingleLevelList(ListTemplate listTemplate)
```

## أمثلة

يوضح كيفية إنشاء قائمة جديدة بمستوى واحد استنادًا إلى القالب المحدد مسبقًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ListCollection listCollection = doc.Lists;

// إنشاء القائمة النقطية من قالب BulletCircle.
List bulletedList = listCollection.AddSingleLevelList(ListTemplate.BulletCircle);

// يكتب القائمة النقطية في المستند الناتج.
builder.Writeln("Bulleted list starts below:");
builder.ListFormat.List = bulletedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// إنشاء القائمة المرقمة من قالب NumberUppercaseLetterDot.
List numberedList = listCollection.AddSingleLevelList(ListTemplate.NumberUppercaseLetterDot);

// يكتب القائمة المرقمة في المستند الناتج.
builder.Writeln("Numbered list starts below:");
builder.ListFormat.List = numberedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Save(ArtifactsDir + "Lists.AddSingleLevelList.docx");
```

### أنظر أيضا

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
