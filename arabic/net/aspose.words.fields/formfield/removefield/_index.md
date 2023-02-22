---
title: FormField.RemoveField
second_title: Aspose.Words لمراجع .NET API
description: FormField طريقة. يزيل حقل النموذج بالكامل  وليس فقط الحرف الخاص لحقل النموذج.
type: docs
weight: 240
url: /ar/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

يزيل حقل النموذج بالكامل ، وليس فقط الحرف الخاص لحقل النموذج.

```csharp
public void RemoveField()
```

### ملاحظات

إذا كانت هناك إشارة مرجعية مرتبطة بحقل النموذج ، فلن تتم إزالة الإشارة المرجعية .

### أمثلة

يوضح كيفية حذف حقل نموذج.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### أنظر أيضا

* class [FormField](../)
* مساحة الاسم [Aspose.Words.Fields](../../formfield/)
* المجسم [Aspose.Words](../../../)


