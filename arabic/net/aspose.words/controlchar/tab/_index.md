---
title: ControlChar.Tab
second_title: Aspose.Words لمراجع .NET API
description: ControlChar مجال. حرف علامة التبويب x0009 أو t.
type: docs
weight: 270
url: /ar/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

حرف علامة التبويب: "\x0009" أو "\t".

```csharp
public static readonly string Tab;
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

* class [ControlChar](../)
* مساحة الاسم [Aspose.Words](../../controlchar/)
* المجسم [Aspose.Words](../../../)


