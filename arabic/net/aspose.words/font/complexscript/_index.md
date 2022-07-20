---
title: ComplexScript
second_title: Aspose.Words لمراجع .NET API
description: يحدد ما إذا كان يجب معاملة محتويات هذا التشغيل كنص نص برمجي معقد بغض النظر عن قيم أحرف Unicode الخاصة بها عند تحديد تنسيق هذا التشغيل.
type: docs
weight: 80
url: /ar/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

يحدد ما إذا كان يجب معاملة محتويات هذا التشغيل كنص نص برمجي معقد بغض النظر عن قيم أحرف Unicode الخاصة بها عند تحديد تنسيق هذا التشغيل.

```csharp
public bool ComplexScript { get; set; }
```

### أمثلة

يوضح كيفية إضافة نص يتم التعامل معه دائمًا على أنه برنامج نصي معقد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### أنظر أيضا

* class [Font](../../font)
* مساحة الاسم [Aspose.Words](../../font)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->