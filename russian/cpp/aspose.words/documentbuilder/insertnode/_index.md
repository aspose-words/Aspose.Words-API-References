---
title: "Aspose::Words::DocumentBuilder::InsertNode метод"
linktitle: "InsertNode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertNode метод. Вставляет узел перед курсором в C++."
type: docs
weight: 40000
url: /ru/cpp/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder::InsertNode method


Вставляет узел перед курсором.

```cpp
void Aspose::Words::DocumentBuilder::InsertNode(const System::SharedPtr<Aspose::Words::Node> &node)
```


## Примеры



Показывает, как вставить привязанное изображение в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// Ниже представлены два способа применения изображения к фигуре, чтобы она могла его отображать.
// 1 - Установите фигуру так, чтобы она содержала изображение.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// Каждое изображение, которое мы сохраняем в фигуре, увеличивает размер нашего документа.
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 - Установите фигуру так, чтобы она ссылалась на файл изображения в локальной файловой системе.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// Привязка к изображениям экономит место и приводит к меньшему размеру документа.
// Однако документ может корректно отображать изображение только пока
// файл изображения присутствует по пути, на который указывает свойство \"SourceFullName\" фигуры.
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## См. также

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
