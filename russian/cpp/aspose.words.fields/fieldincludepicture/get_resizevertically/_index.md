---
title: "Метод Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically"
linktitle: "get_ResizeVertically"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically. Получает или задает, следует ли изменять размер изображения по вертикали из источника в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.fields/fieldincludepicture/get_resizevertically/
---
## FieldIncludePicture::get_ResizeVertically method


Получает или задает, следует ли изменять размер изображения по вертикали из исходного файла.

```cpp
bool Aspose::Words::Fields::FieldIncludePicture::get_ResizeVertically()
```


## Примеры



Показывает, как вставлять изображения с помощью полей IMPORT и INCLUDEPICTURE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два похожих типа полей, которые мы можем использовать для отображения изображений, связанных из локальной файловой системы.
// 1 -  Поле INCLUDEPICTURE:
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// Примените фильтр PNG32.FLT.
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  Поле IMPORT:
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## См. также

* Class [FieldIncludePicture](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
