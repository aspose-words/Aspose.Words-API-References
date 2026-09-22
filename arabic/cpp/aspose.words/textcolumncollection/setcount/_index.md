---
title: "Aspose::Words::TextColumnCollection::SetCount طريقة"
linktitle: "SetCount"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TextColumnCollection::SetCount طريقة. يرتب النص في عدد محدد من الأعمدة النصية في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection::SetCount method


ينظم النص في عدد محدد من الأعمدة النصية.

```cpp
void Aspose::Words::TextColumnCollection::SetCount(int32_t newCount)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| newCount | int32_t | عدد الأعمدة التي سيتم ترتيب النص فيها. |
## ملاحظات


عندما تكون [EvenlySpaced](../get_evenlyspaced/) **false** وتزيد عدد الأعمدة، يتم إنشاء كائنات [TextColumn](../../textcolumn/) جديدة بعرض وتباعد صفر. تحتاج إلى تعيين العرض والتباعد للأعمدة الجديدة.

## أمثلة



يوضح كيفية إنشاء أعمدة متعددة موزعة بالتساوي في قسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## انظر أيضًا

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
