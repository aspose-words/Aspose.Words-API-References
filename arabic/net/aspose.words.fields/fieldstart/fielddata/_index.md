---
title: FieldData
second_title: Aspose.Words لمراجع .NET API
description: الحصول على بيانات الحقل المخصصة المرتبطة بالحقل.
type: docs
weight: 10
url: /ar/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

الحصول على بيانات الحقل المخصصة المرتبطة بالحقل.

```csharp
public byte[] FieldData { get; }
```

### أمثلة

يوضح كيفية الحصول على البيانات المرتبطة بالحقل.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.Default.GetString(field.Start.FieldData));
```

### أنظر أيضا

* class [FieldStart](../../fieldstart)
* مساحة الاسم [Aspose.Words.Fields](../../fieldstart)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->