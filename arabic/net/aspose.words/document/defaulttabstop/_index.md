---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تخصيص خاصية DefaultTabStop لتعيين فترات زمنية دقيقة للعلامات التبويبية بالنقاط، مما يؤدي إلى تحسين تنسيق مستندك وتخطيطه.
type: docs
weight: 100
url: /ar/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

يحصل على الفاصل الزمني (بالنقاط) بين علامات التبويب الافتراضية أو يعينه.

```csharp
public double DefaultTabStop { get; set; }
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

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
