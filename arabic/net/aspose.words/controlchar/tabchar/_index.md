---
title: ControlChar.TabChar
linktitle: TabChar
articleTitle: TabChar
second_title: Aspose.Words لـ .NET
description: أتقن استخدام حقول TabChar مع ControlChar لإدارة بيانات سلسة. أطلق العنان لكفاءتك مع حرف Tab متعدد الاستخدامات (char9 أو t) اليوم!
type: docs
weight: 280
url: /ar/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

حرف علامة التبويب: (char)9 أو "\t".

```csharp
public const char TabChar;
```

## أمثلة

يوضح كيفية تعيين فترة زمنية مخصصة لمواضع علامة التبويب.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعيين علامات التبويب لتظهر كل 72 نقطة (1 بوصة).
builder.Document.DefaultTabStop = 72;

// كل حرف علامة تبويب يوجه النص بعده إلى أقرب موضع علامة تبويب.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### أنظر أيضا

* class [ControlChar](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
