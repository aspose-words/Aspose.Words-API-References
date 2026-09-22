---
title: "Aspose::Words::DocumentBuilder::MoveToParagraph method"
linktitle: "MoveToParagraph"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::MoveToParagraph method. ينقل المؤشر إلى فقرة في القسم الحالي في C++."
type: docs
weight: 59000
url: /ar/cpp/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder::MoveToParagraph method


ينقل المؤشر إلى فقرة في القسم الحالي.

```cpp
void Aspose::Words::DocumentBuilder::MoveToParagraph(int32_t paragraphIndex, int32_t characterIndex)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| paragraphIndex | int32_t | فهرس الفقرة التي سيتم الانتقال إليها. |
| characterIndex | int32_t | فهرس الحرف داخل الفقرة. القيمة السالبة تسمح لك بتحديد موقع من نهاية الفقرة. استخدم -1 للانتقال إلى نهاية الفقرة. |
## ملاحظات


The navigation is performed inside the current story of the current section. أي إذا قمت بنقل المؤشر إلى العنوان الرئيسي للقسم الأول، فإن *paragraphIndex* يحدد فهرس الفقرة داخل ذلك العنوان لهذا القسم.

عندما يكون *paragraphIndex* أكبر من أو يساوي 0، فإنه يحدد فهرسًا من بداية القسم حيث 0 هو الفقرة الأولى. وعندما يكون *paragraphIndex* أقل من 0، فإنه يحدد فهرسًا من نهاية القسم حيث -1 هو الفقرة الأخيرة.

## أمثلة



يوضح كيفية نقل موضع مؤشر المُنشئ إلى فقرة محددة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(22, paragraphs->get_Count());

// إنشاء مُنشئ مستند لتعديل المستند. مؤشر المُنشئ،
// وهو النقطة التي سيُدرج فيها العقد الجديدة عندما نستدعي طرق بناء المستند الخاصة به،
// حاليًا في بداية المستند.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_EQ(0, paragraphs->IndexOf(builder->get_CurrentParagraph()));

// نقل ذلك المؤشر إلى فقرة مختلفة سيضع المؤشر أمام تلك الفقرة.
builder->MoveToParagraph(2, 0);

// أي محتوى جديد نضيفه سيُدرج في تلك النقطة.
builder->Writeln(u"This is a new third paragraph. ");
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
