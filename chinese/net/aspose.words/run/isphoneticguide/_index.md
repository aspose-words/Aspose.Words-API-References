---
title: Run.IsPhoneticGuide
second_title: Aspose.Words for .NET API 参考
description: Run 财产. 获取一个布尔值指示该运行是语音指南
type: docs
weight: 20
url: /zh/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

获取一个布尔值，指示该运行是语音指南。

```csharp
public bool IsPhoneticGuide { get; }
```

### 例子

演示如何获取拼音指南的属性。

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");            

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// 在亚洲文本中使用拼音指南。
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### 也可以看看

* class [Run](../)
* 命名空间 [Aspose.Words](../../run/)
* 部件 [Aspose.Words](../../../)


