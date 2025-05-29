---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words لـ .NET
description: قم بإلغاء قفل بيانات الحقل المخصصة باستخدام خاصية FieldData في FieldStart، مما يعمل على تحسين إدارة البيانات لديك وتعزيز الإنتاجية بسهولة.
type: docs
weight: 10
url: /ar/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

يحصل على بيانات الحقل المخصصة المرتبطة بالحقل.

```csharp
public byte[] FieldData { get; }
```

## أمثلة

يوضح كيفية الحصول على البيانات المرتبطة بالحقل.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.UTF8.GetString(field.Start.FieldData));
```

### أنظر أيضا

* class [FieldStart](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
