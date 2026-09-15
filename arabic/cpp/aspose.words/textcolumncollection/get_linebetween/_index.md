---
title: "Aspose::Words::TextColumnCollection::get_LineBetween طريقة"
linktitle: "get_LineBetween"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TextColumnCollection::get_LineBetween طريقة. عندما تكون true، يضيف خطًا عموديًا بين الأعمدة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/textcolumncollection/get_linebetween/
---
## TextColumnCollection::get_LineBetween method


عند **true**، يضيف خطًا عموديًا بين الأعمدة.

```cpp
bool Aspose::Words::TextColumnCollection::get_LineBetween()
```


## أمثلة



يعرض كيفية فصل الأعمدة بخط عمودي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// قم بتكوين كائن PageSetup للقسم الحالي لتقسيم النص إلى عدة أعمدة.
// قم بتعيين الخاصية "LineBetween" إلى "true" لوضع خط فاصل بين الأعمدة.
// قم بتعيين الخاصية "LineBetween" إلى "false" لترك المسافة بين الأعمدة فارغة.
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_LineBetween(lineBetween);
columns->SetCount(3);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 3.");

doc->Save(get_ArtifactsDir() + u"PageSetup.VerticalLineBetweenColumns.docx");
```

## انظر أيضًا

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
