---
title: Document.DefaultTabStop
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. الحصول على الفاصل الزمني بالنقاط أو تعيينه بين علامات الجدولة الافتراضية.
type: docs
weight: 90
url: /ar/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

الحصول على الفاصل الزمني (بالنقاط) أو تعيينه بين علامات الجدولة الافتراضية.

```csharp
public double DefaultTabStop { get; set; }
```

### أمثلة

يوضح كيفية تعيين فاصل زمني مخصص لمواضع علامات الجدولة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتعيين علامات الجدولة لتظهر كل 72 نقطة (1 بوصة).
builder.Document.DefaultTabStop = 72;

// يلتقط كل حرف جدولة النص الذي يليه إلى أقرب موضع لعلامة الجدولة.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### أنظر أيضا

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


