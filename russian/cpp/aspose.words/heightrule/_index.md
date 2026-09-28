---
title: "Aspose::Words::HeightRule enum"
linktitle: "HeightRule"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::HeightRule enum. Указывает правило определения высоты объекта в C++."
type: docs
weight: 91000
url: /ru/cpp/aspose.words/heightrule/
---
## HeightRule enum


Указывает правило определения высоты объекта.

```cpp
enum class HeightRule
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| AtLeast | 0 | Высота будет как минимум указанной высоты в пунктах. При необходимости она будет увеличиваться, чтобы вместить весь текст внутри объекта. |
| Exactly | 1 | Высота задаётся точно в пунктах. Обратите внимание, что если текст не поместится в объект этой высоты, он будет обрезан. |
| Авто | 2 | Высота будет автоматически увеличиваться, чтобы вместить весь текст внутри объекта. |


## Примеры



Показывает, как форматировать строки с помощью Document Builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Начните вторую строку, а затем настройте её высоту. Builder применит эти настройки к
// текущей строке, а также всем новым строкам, которые он создаст позже.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// Первая строка не пострадала от переустановки отступов и по‑прежнему содержит значения по умолчанию.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
