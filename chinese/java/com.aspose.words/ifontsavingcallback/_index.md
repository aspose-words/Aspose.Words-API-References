---
title: IFontSavingCallback
second_title: Aspose.Words for Java API 参考
description: 如果您想接收通知并控制 Aspose.Words 在将文档导出为 HTML 格式时如何保存字体，请实现此接口。
type: docs
weight: 646
url: /zh/java/com.aspose.words/ifontsavingcallback/
---
```
public interface IFontSavingCallback
```

如果您想接收通知并控制 Aspose.Words 在将文档导出为 HTML 格式时如何保存字体，请实现此接口。
## 方法

| 方法 | 描述 |
| --- | --- |
| [fontSaving(FontSavingArgs args)](#fontSaving-com.aspose.words.FontSavingArgs-) | 当 Aspose.Words 将要保存字体资源时调用。 |
### fontSaving(FontSavingArgs args) {#fontSaving-com.aspose.words.FontSavingArgs-}
```
public abstract void fontSaving(FontSavingArgs args)
```


当 Aspose.Words 将要保存字体资源时调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [FontSavingArgs](../../com.aspose.words/fontsavingargs) |  |
