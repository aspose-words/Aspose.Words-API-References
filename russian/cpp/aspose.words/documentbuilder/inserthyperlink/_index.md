---
title: "Aspose::Words::DocumentBuilder::InsertHyperlink метод"
linktitle: "InsertHyperlink"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertHyperlink метод. Вставляет гиперссылку в документ в C++."
type: docs
weight: 38000
url: /ru/cpp/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder::InsertHyperlink method


Вставляет гиперссылку в документ.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertHyperlink(const System::String &displayText, const System::String &urlOrBookmark, bool isBookmark)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| displayText | const System::String\& | Текст ссылки, отображаемый в документе. |
| urlOrBookmark | const System::String\& | Назначение ссылки. Может быть URL или именем закладки внутри документа. Этот метод всегда добавляет апострофы в начале и в конце URL. |
| isBookmark | bool | **true** если предыдущий параметр является именем закладки внутри документа; **false** если предыдущий параметр является URL. |

### ReturnValue

Объект [Field](../../../aspose.words.fields/field/), представляющий вставленное поле.
## Примечания


Обратите внимание, что вам необходимо явно указать форматирование шрифта для отображаемого текста гиперссылки, используя свойство [Font](../get_font/).

Этот метод внутри вызывает [InsertField()](../), чтобы вставить поле HYPERLINK MS Word в документ.

## Примеры



Показывает, как вставить поле гиперссылки.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Вставьте гиперссылку и выделите её с помощью пользовательского форматирования.
// Гиперссылка будет кликабельным фрагментом текста, который перенаправит нас к месту, указанному в URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + щелчок левой кнопкой мыши по ссылке в тексте в Microsoft Word откроет URL в новом окне веб‑браузера.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


Показывает, как использовать стек форматирования построителя документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Настройте форматирование шрифта, затем запишите текст, который будет перед гиперссылкой.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Сохраните текущую конфигурацию форматирования в стеке.
builder->PushFont();

// Измените текущее форматирование построителя, применив новый стиль.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Восстановите сохранённое ранее форматирование шрифта и удалите элемент из стека.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```


Показывает, как вставить гиперссылку, ссылающуюся на локальную закладку.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Вставьте поле HYPERLINK, которое ссылается на закладку. Мы можем передать переключатели поля
// в метод "InsertHyperlink" в качестве части аргумента, содержащего имя ссылочной закладки.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## См. также

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
