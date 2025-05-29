---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font ComplexScript، مما يضمن تنسيق النص الخاص بك كنص معقد لتحسين قابلية القراءة والأسلوب، بغض النظر عن قيم Unicode.
type: docs
weight: 80
url: /ar/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

يحدد ما إذا كان سيتم التعامل مع محتويات هذا التشغيل كنص نصي معقد بغض النظر عن قيم أحرف Unicode الخاصة بها عند تحديد التنسيق لهذا التشغيل.

```csharp
public bool ComplexScript { get; set; }
```

## أمثلة

يوضح كيفية إضافة نص يتم التعامل معه دائمًا على أنه نص معقد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
