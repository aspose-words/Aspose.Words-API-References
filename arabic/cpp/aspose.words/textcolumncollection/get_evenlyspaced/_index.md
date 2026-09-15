---
title: "طريقة Aspose::Words::TextColumnCollection::get_EvenlySpaced"
linktitle: "get_EvenlySpaced"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::TextColumnCollection::get_EvenlySpaced. صحيح إذا كانت أعمدة النص ذات عرض متساوٍ ومتباعدة بالتساوي في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/textcolumncollection/get_evenlyspaced/
---
## TextColumnCollection::get_EvenlySpaced method


صحيح إذا كانت أعمدة النص ذات عرض متساوٍ وموزعة بالتساوي.

```cpp
bool Aspose::Words::TextColumnCollection::get_EvenlySpaced()
```


## أمثلة



يظهر كيفية إنشاء أعمدة ذات تباعد غير متساوٍ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// حدد مقدار المساحة المتاحة لدينا لترتيب الأعمدة.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// اجعل العمود الأول ضيقًا.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// اجعل العمود الثاني يأخذ باقي المساحة المتاحة داخل هوامش الصفحة.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## انظر أيضًا

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
