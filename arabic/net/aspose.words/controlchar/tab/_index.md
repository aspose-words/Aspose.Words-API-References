---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: Aspose.Words لـ .NET
description: اكتشف حقل علامة التبويب ControlChar، وفهم حرف Tab x0009 لتحقيق تنسيق نصي فعال وإدارة بيانات محسنة.
type: docs
weight: 270
url: /ar/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

حرف علامة التبويب: "\x0009" أو "\t".

```csharp
public static readonly string Tab;
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
