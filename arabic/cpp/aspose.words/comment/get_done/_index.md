---
title: "طريقة Aspose::Words::Comment::get_Done"
linktitle: "get_Done"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Comment::get_Done. يحصل أو يعيّن العلم الذي يشير إلى أن التعليق تم وضع علامة تم إنجازه في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/comment/get_done/
---
## Comment::get_Done method


يحصل أو يعيّن علامة تشير إلى أن التعليق تم وضع علامة done عليه.

```cpp
bool Aspose::Words::Comment::get_Done() const
```


## أمثلة



يوضح كيفية وضع علامة "done" على التعليق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// أدرج تعليقًا لتوضيح خطأ.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// التعليقات تحتوي على علم "Done"، والذي يُضبط على "false" افتراضيًا.
// إذا اقترح تعليق أننا نجري تغييرًا داخل المستند،
// يمكننا تطبيق التغيير، ثم ضبط علم "Done" لاحقًا للإشارة إلى التصحيح.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// التعليقات التي تم وضع علامة "done" عليها ستميز نفسها.
// من العناصر التي ليست "مكتملة" بل بلون نص باهت.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## انظر أيضًا

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
