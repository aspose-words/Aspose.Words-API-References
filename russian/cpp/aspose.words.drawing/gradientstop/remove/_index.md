---
title: "Метод Aspose::Words::Drawing::GradientStop::Remove"
linktitle: "Remove"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::GradientStop::Remove. Удаляет градиентную остановку из родительского GradientStopCollection в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.drawing/gradientstop/remove/
---
## GradientStop::Remove method


Удаляет градиентную остановку из родительского [GradientStopCollection](../../gradientstopcollection/).

```cpp
void Aspose::Words::Drawing::GradientStop::Remove()
```


## Примеры



Показывает, как добавить остановки градиента к заливке градиентом.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
shape->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Green(), System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2);

// Получить коллекцию остановок градиента.
System::SharedPtr<Aspose::Words::Drawing::GradientStopCollection> gradientStops = shape->get_Fill()->get_GradientStops();

// Изменить первую остановку градиента.
gradientStops->idx_get(0)->set_Color(System::Drawing::Color::get_Aqua());
gradientStops->idx_get(0)->set_Position(0.1);
gradientStops->idx_get(0)->set_Transparency(0.25);

// Добавить новую остановку градиента в конец коллекции.
auto gradientStop = System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Brown(), 0.5);
gradientStops->Add(gradientStop);

// Удалить остановку градиента по индексу 1.
gradientStops->RemoveAt(1);
// И вставить новую остановку градиента по тому же индексу 1.
gradientStops->Insert(1, System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Chocolate(), 0.75, 0.3));

// Удалить последнюю остановку градиента в коллекции.
gradientStop = gradientStops->idx_get(2);
gradientStops->Remove(gradientStop);

ASSERT_EQ(2, gradientStops->get_Count());

ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 0, 255, 255), gradientStops->idx_get(0)->get_BaseColor());
ASSERT_EQ(System::Drawing::Color::get_Aqua().ToArgb(), gradientStops->idx_get(0)->get_Color().ToArgb());
ASSERT_NEAR(0.1, gradientStops->idx_get(0)->get_Position(), 0.01);
ASSERT_NEAR(0.25, gradientStops->idx_get(0)->get_Transparency(), 0.01);

ASSERT_EQ(System::Drawing::Color::get_Chocolate().ToArgb(), gradientStops->idx_get(1)->get_Color().ToArgb());
ASSERT_NEAR(0.75, gradientStops->idx_get(1)->get_Position(), 0.01);
ASSERT_NEAR(0.3, gradientStops->idx_get(1)->get_Transparency(), 0.01);

// Используйте параметр совместимости, чтобы определить форму с помощью DML
// если вы хотите получить свойство "GradientStops" после сохранения документа.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientStops.docx", saveOptions);
```

## См. также

* Class [GradientStop](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
