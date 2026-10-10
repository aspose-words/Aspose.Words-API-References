---
title: "Aspose::Words::TextColumn::get_SpaceAfter طريقة"
linktitle: "get_SpaceAfter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TextColumn::get_SpaceAfter طريقة. يحصل على أو يضبط المسافة بين هذا العمود والعمود التالي بالنقاط. غير مطلوب للعمود الأخير في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/textcolumn/get_spaceafter/
---
## TextColumn::get_SpaceAfter method


يحصل أو يضبط المسافة بين هذا العمود والعمود التالي بالنقاط. غير مطلوب للعمود الأخير.

```cpp
double Aspose::Words::TextColumn::get_SpaceAfter()
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

* Class [TextColumn](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
