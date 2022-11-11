---
title: IDocumentPartSavingCallback
second_title: Aspose.Words for Java API 参考
description: 如果您想接收通知并控制 Aspose.Words 在将文档导出为或格式化时如何保存文档部分，请实施此接口。
type: docs
weight: 637
url: /zh/java/com.aspose.words/idocumentpartsavingcallback/
---
```
public interface IDocumentPartSavingCallback
```

如果您想接收通知并控制 Aspose.Words 在将文档导出到[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML)或者[SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)格式。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [documentPartSaving(DocumentPartSavingArgs args)](#documentPartSaving-com.aspose.words.DocumentPartSavingArgs-) | 当 Aspose.Words 即将保存文档部分时调用。 |
### documentPartSaving(DocumentPartSavingArgs args) {#documentPartSaving-com.aspose.words.DocumentPartSavingArgs-}
```
public abstract void documentPartSaving(DocumentPartSavingArgs args)
```


当 Aspose.Words 即将保存文档部分时调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [DocumentPartSavingArgs](../../com.aspose.words/documentpartsavingargs) |  |
