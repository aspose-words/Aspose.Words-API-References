---
title: ProtectionType Enum
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.ProtectionType enum لضمان أمان مستندات قوي. حسّن مستنداتك بخيارات حماية قابلة للتخصيص اليوم!
type: docs
weight: 5240
url: /ar/net/aspose.words/protectiontype/
---
## ProtectionType enumeration

نوع الحماية للمستند.

```csharp
public enum ProtectionType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| AllowOnlyComments | `1` | يمكن للمستخدم تعديل التعليقات في المستند فقط. |
| AllowOnlyFormFields | `2` | يمكن للمستخدم إدخال البيانات فقط في حقول النموذج الموجودة في المستند. |
| AllowOnlyRevisions | `0` | يمكن للمستخدم فقط إضافة علامات المراجعة إلى المستند. |
| ReadOnly | `3` | لا يُسمح بإجراء أي تعديلات على المستند. متوفر منذ إصدار Microsoft Word 2003. |
| NoProtection | `-1` | المستند غير محمي. |

## أمثلة

يوضح كيفية إيقاف الحماية لقسم ما.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// تطبيق الحماية ضد الكتابة على كل قسم في المستند.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// قم بإيقاف تشغيل الحماية ضد الكتابة للقسم الأول.
doc.Sections[0].ProtectedForForms = false;

// في وثيقة الإخراج هذه، سنكون قادرين على تحرير القسم الأول بحرية،
// ولن نتمكن من تحرير محتويات حقل النموذج إلا في القسم الثاني.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
