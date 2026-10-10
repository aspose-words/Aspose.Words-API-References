---
title: "Aspose::Words::FileCorruptedException typedef"
linktitle: "FileCorruptedException"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::FileCorruptedException typedef. يتم إلقاؤه أثناء تحميل المستند، عندما يبدو المستند تالفًا ولا يمكن تحميله. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 133000
url: /ar/cpp/aspose.words/filecorruptedexception/
---
## FileCorruptedException typedef


يُطرح أثناء تحميل المستند، عندما يبدو المستند تالفًا ولا يمكن تحميله. لمعرفة المزيد، زر مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
using Aspose::Words::FileCorruptedException = typedef System::ExceptionWrapper<Details_FileCorruptedException>
```


## أمثلة



يظهر كيفية التقاط استثناء FileCorruptedException.
```cpp
try
{
    // إذا حصلنا على رسالة الخطأ "Unreadable content" عند محاولة فتح مستند باستخدام Microsoft Word،
    // فمن المحتمل أن يتم إلقاء استثناء عند محاولة تحميل ذلك المستند باستخدام Aspose.Words.
    auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted document.docx");
}
catch (Aspose::Words::FileCorruptedException& e)
{
    std::cout << e->get_Message() << std::endl;
}
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
