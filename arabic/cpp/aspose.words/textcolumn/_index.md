---
title: "فئة Aspose::Words::TextColumn"
linktitle: "TextColumn"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::TextColumn. تمثل عمود نص واحد. TextColumn هو عضو في مجموعة TextColumnCollection. تشمل مجموعة TextColumn جميع الأعمدة في قسم من المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 70000
url: /ar/cpp/aspose.words/textcolumn/
---
## TextColumn class


يمثل عمود نص واحد. [TextColumn](./) هو عضو في مجموعة [TextColumnCollection](../textcolumncollection/). تشمل مجموعة [TextColumn](./) جميع الأعمدة في قسم من مستند. لمعرفة المزيد، زر مقالة الوثائق [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumn : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_SpaceAfter](./get_spaceafter/)() | يحصل أو يضبط المسافة بين هذا العمود والعمود التالي بالنقاط. غير مطلوب للعمود الأخير. |
| [get_Width](./get_width/)() | يحصل أو يضبط عرض عمود النص بالنقاط. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SpaceAfter](./set_spaceafter/)(double) | مُعيّن لـ [Aspose::Words::TextColumn::get_SpaceAfter](./get_spaceafter/). |
| [set_Width](./set_width/)(double) | مُعيّن لـ [Aspose::Words::TextColumn::get_Width](./get_width/). |
| static [Type](./type/)() |  |
## ملاحظات


[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns.[EvenlySpaced](../textcolumncollection/get_evenlyspaced/) to **true**.

عند إنشاء [TextColumn](./) جديد يتم تعيين عرضه وتباعده إلى الصفر.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
