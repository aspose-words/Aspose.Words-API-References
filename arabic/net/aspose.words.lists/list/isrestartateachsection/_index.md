---
title: List.IsRestartAtEachSection
linktitle: IsRestartAtEachSection
articleTitle: IsRestartAtEachSection
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsRestartAtEachSection للتحكم في ترقيم القوائم في الأقسام. حسّن تنظيم المستندات بهذه الميزة سهلة الاستخدام!
type: docs
weight: 50
url: /ar/net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

يحدد ما إذا كان يجب إعادة تشغيل القائمة في كل قسم. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IsRestartAtEachSection { get; set; }
```

## ملاحظات

يتم دعم هذا الخيار فقط في تنسيقات المستندات RTF وDOC وDOCX.

سيتم كتابة هذا الخيار إلى DOCX فقط إذا[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/) أعلى من ذلكEcma376_2006.

## أمثلة

يوضح كيفية تكوين قائمة لإعادة تشغيل الترقيم في كل قسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// سيتم تطبيق خاصية "IsRestartAtEachSection" فقط عندما
// مستوى توافق OOXML الخاص بالمستند هو معيار أحدث من "OoxmlComplianceCore.Ecma376".
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

### أنظر أيضا

* class [List](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
