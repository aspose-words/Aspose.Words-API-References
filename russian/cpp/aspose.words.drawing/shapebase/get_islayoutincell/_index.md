---
title: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell метод"
linktitle: "get_IsLayoutInCell"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell метод. Получает или задает флаг, указывающий, отображается ли фигура внутри таблицы или вне её в C++."
type: docs
weight: 32000
url: /ru/cpp/aspose.words.drawing/shapebase/get_islayoutincell/
---
## ShapeBase::get_IsLayoutInCell method


Получает или задает флаг, указывающий, отображается ли фигура внутри таблицы или снаружи.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell()
```

## Примечания


Значение по умолчанию — **true**.

Имеет эффект только для фигур верхнего уровня, свойство [WrapType](../get_wraptype/) которых установлено в значение, отличное от [Inline](../../../aspose.words/inline/).

## Примеры



Показывает, как определить, как отображать фигуру в ячейке таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(10);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table->set_Style(tableStyle);

builder->MoveTo(table->get_FirstRow()->get_FirstCell()->get_FirstParagraph());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);

// Установите свойство "IsLayoutInCell" в "true", чтобы отображать фигуру как встроенный элемент внутри абзаца ячейки.
// Начало координат, определяющее расположение фигуры, будет в левом верхнем углу ячейки фигуры.
// Если мы изменим размер ячейки, фигура переместится, чтобы сохранить то же положение, начиная с левого верхнего угла ячейки.
// Установите свойство "IsLayoutInCell" в "false", чтобы отображать фигуру как независимую плавающую фигуру.
// Начало координат, определяющее расположение фигуры, будет в левом верхнем углу страницы,
// и фигура не будет реагировать на изменение размера её ячейки.
shape->set_IsLayoutInCell(isLayoutInCell);

// Мы можем применять свойство "IsLayoutInCell" только к плавающим фигурам.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

doc->Save(get_ArtifactsDir() + u"Shape.LayoutInTableCell.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
