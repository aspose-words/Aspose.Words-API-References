---
title: "Aspose::Words::FileCorruptedException typedef"
linktitle: "FileCorruptedException"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileCorruptedException typedef. 在文档加载期间抛出，当文档似乎已损坏且无法加载时。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 133000
url: /zh/cpp/aspose.words/filecorruptedexception/
---
## FileCorruptedException typedef


在文档加载期间抛出，当文档似乎已损坏且无法加载时。要了解更多，请访问[Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/)文档文章。

```cpp
using Aspose::Words::FileCorruptedException = typedef System::ExceptionWrapper<Details_FileCorruptedException>
```


## 示例



展示如何捕获 FileCorruptedException。
```cpp
try
{
    // 如果在使用 Microsoft Word 打开文档时收到 "Unreadable content" 错误消息，
    // 则很可能在使用 Aspose.Words 加载该文档时抛出异常。
    auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted document.docx");
}
catch (Aspose::Words::FileCorruptedException& e)
{
    std::cout << e->get_Message() << std::endl;
}
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
