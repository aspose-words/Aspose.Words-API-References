---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: Aspose.Words لـ .NET
description: FormField RemoveField طريقة. إزالة حقل النموذج بالكامل وليس فقط الحرف الخاص لحقل النموذج في C#.
type: docs
weight: 240
url: /ar/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

إزالة حقل النموذج بالكامل، وليس فقط الحرف الخاص لحقل النموذج.

```csharp
public void RemoveField()
```

## ملاحظات

إذا كانت هناك إشارة مرجعية مرتبطة بحقل النموذج، فلن تتم إزالة الإشارة المرجعية.

## أمثلة

يوضح كيفية حذف حقل النموذج.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### أنظر أيضا

* class [FormField](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
