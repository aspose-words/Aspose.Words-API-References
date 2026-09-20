---
title: "Aspose::Words::StyleCollection::AddCopy метод"
linktitle: "AddCopy"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::StyleCollection::AddCopy метод. Копирует стиль в эту коллекцию в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/stylecollection/addcopy/
---
## StyleCollection::AddCopy method


Копирует стиль в эту коллекцию.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::AddCopy(const System::SharedPtr<Aspose::Words::Style> &style)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| style | const System::SharedPtr\<Aspose::Words::Style\>\& | [Style](../../style/) для копирования. |

### ReturnValue

Скопированный стиль готов к использованию.
## Примечания


[Style](../../style/) to be copied can belong to the same document as well as to different document.

Связанный стиль скопирован.

Этот метод не копирует базовые стили.

Если коллекция уже содержит стиль с тем же именем, то новое имя автоматически генерируется путем добавления суффикса "_number", начиная с 0, например "Normal_0", "Heading 1_1" и т.д. Используйте сеттер [Name](../../style/get_name/) для изменения имени импортированного стиля.

## Примеры



Показывает, как клонировать стиль документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Метод AddCopy создает копию указанного стиля и
// автоматически генерирует новое имя для стиля, например "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Используйте свойство "Name" стиля, чтобы изменить идентифицирующее имя стиля.
newStyle->set_Name(u"My Heading 1");

// В нашем документе теперь есть два визуально одинаковых стиля с разными именами.
// Изменение настроек одного из стилей не влияет на другой.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```


Показывает, как импортировать стиль из одного документа в другой документ.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

// Создайте пользовательский стиль для исходного документа.
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
srcStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Импортируйте пользовательский стиль исходного документа в целевой документ.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> newStyle = dstDoc->get_Styles()->AddCopy(srcStyle);

// Импортированный стиль имеет внешний вид, идентичный его исходному стилю.
ASSERT_EQ(u"MyStyle", newStyle->get_Name());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), newStyle->get_Font()->get_Color().ToArgb());
```

## См. также

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
