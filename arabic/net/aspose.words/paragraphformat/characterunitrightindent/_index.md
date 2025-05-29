---
title: ParagraphFormat.CharacterUnitRightIndent
linktitle: CharacterUnitRightIndent
articleTitle: CharacterUnitRightIndent
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParagraphFormat CharacterUnitRightIndent لتعديل قيم المسافة البادئة اليمنى للأحرف في فقراتك بسهولة، مما يؤدي إلى تحسين تخطيط مستندك.
type: docs
weight: 90
url: /ar/net/aspose.words/paragraphformat/characterunitrightindent/
---
## ParagraphFormat.CharacterUnitRightIndent property

يحصل على قيمة المسافة البادئة الصحيحة (بالأحرف) للفقرات المحددة أو يعينها.

```csharp
public double CharacterUnitRightIndent { get; set; }
```

## أمثلة

يوضح كيفية تغيير المسافة بين الفقرات والمسافات البادئة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// فيما يلي خمسة خيارات مختلفة للتباعد، بالإضافة إلى الخصائص التي يؤثر عليها تكوينها بشكل غير مباشر.
// 1 - المسافة البادئة اليسرى:
Assert.AreEqual(format.LeftIndent, 0.0d);

format.CharacterUnitLeftIndent = 10.0;

Assert.AreEqual(format.LeftIndent, 120.0d);

// 2 - المسافة البادئة اليمنى:
Assert.AreEqual(format.RightIndent, 0.0d); 

format.CharacterUnitRightIndent = -5.5;

Assert.AreEqual(format.RightIndent, -66.0d);

// 3 - المسافة البادئة المعلقة:
Assert.AreEqual(format.FirstLineIndent, 0.0d);

format.CharacterUnitFirstLineIndent = 20.3;

Assert.AreEqual(format.FirstLineIndent, 243.59d, 0.1d);

// 4 - المسافة بين الأسطر قبل الفقرات:
Assert.AreEqual(format.SpaceBefore, 0.0d);

format.LineUnitBefore = 5.1;

Assert.AreEqual(format.SpaceBefore, 61.1d, 0.1d);

// 5 - المسافة بين الأسطر بعد الفقرات:
Assert.AreEqual(format.SpaceAfter, 0.0d);

format.LineUnitAfter = 10.9;

Assert.AreEqual(format.SpaceAfter, 130.8d, 0.1d);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试" +
              "文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
